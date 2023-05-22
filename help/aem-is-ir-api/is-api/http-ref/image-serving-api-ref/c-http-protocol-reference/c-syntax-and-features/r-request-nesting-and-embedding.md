---
description: 이미지 제공에서는 이미지 제공 요청의 무제한 중첩, 이미지 렌더링 요청의 포함, 외부 서버에서 검색된 이미지의 포함 등을 지원합니다. 이러한 메커니즘은 레이어 이미지 및 레이어 마스크만 지원합니다.
solution: Experience Manager
title: 중첩 및 포함 요청
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 0%

---

# 중첩 및 포함 요청{#request-nesting-and-embedding}

이미지 제공에서는 이미지 제공 요청의 무제한 중첩, 이미지 렌더링 요청의 포함, 외부 서버에서 검색된 이미지의 포함 등을 지원합니다. 이러한 메커니즘은 레이어 이미지 및 레이어 마스크만 지원합니다.

>[!NOTE]
>
>특정 이메일 클라이언트와 프록시 서버는 중첩 및 포함 구문에 사용되는 중괄호를 인코딩할 수 있습니다. 이 문제가 있는 응용 프로그램에서는 중괄호 대신 괄호를 사용해야 합니다.

## 중첩 이미지 제공 요청 {#section-6954202119e0466f8ff27c79f4f039c8}

전체 이미지 제공 요청은에서 지정하여 레이어 소스로 사용할 수 있습니다. `src=` (또는 `mask=`) 다음 구문을 사용하는 명령입니다.

`…&src=is( nestedRequest)&…`

다음 `is` 토큰은 대/소문자를 구분합니다.

중첩 요청에는 서버 루트 경로가 포함되지 않아야 합니다(일반적으로). ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>중첩된 요청 구분 기호 문자( `'(',')'`) 및 명령 구분 기호 문자( `'?'`, `'&'`, `'='`중첩된 요청 내에서 는 HTTP 인코딩이 아니어야 합니다. 사실상, 중첩된 요청은 외부(중첩) 요청과 동일하게 인코딩해야 합니다.

사전 처리 규칙은 중첩 요청에 적용됩니다.

다음 명령은 중첩 요청(요청 URL 또는 )에 지정될 때 무시됩니다 `catalog::Modifier` 또는 `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

중첩된 요청의 결과 이미지에 마스크(알파) 데이터가 포함된 경우 레이어 마스크로 포함 레이어에 전달됩니다.

또한 무시됩니다. `attribute::MaxPix`및 `attribute::DefaultPix` 중첩된 요청에 적용되는 이미지 카탈로그의 수입니다.

중첩된 IS 요청의 이미지 결과는 다음을 포함하여 선택적으로 캐시할 수 있습니다. `cache=on`. 기본적으로 중간 데이터의 캐싱은 비활성화되어 있습니다. 적절한 기간 내에 중간 이미지를 다른 요청에서 재사용할 것으로 예상되는 경우에만 캐싱을 활성화해야 합니다. 표준 서버측 캐시 관리가 적용됩니다. 데이터는 무손실 형식으로 캐시됩니다.

## 포함된 이미지 렌더링 요청 {#section-69c5548db930412b9b90d9b2951a6969}

서버에서 Dynamic Media 이미지 렌더링이 활성화되면 src=(또는 mask=) 명령에서 렌더링 요청을 지정하여 레이어 소스로 사용할 수 있습니다. 다음 구문을 사용합니다.

` …&src=ir( *[!DNL renderRequest]*)&…`

다음 `ir` 토큰은 대/소문자를 구분합니다.

*[!DNL renderRequest]* 는 HTTP 루트 경로를 제외한 일반적인 이미지 렌더링 요청입니다 ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>중첩된 요청 구분 기호 문자( `'(',')'`) 및 명령 구분 기호 문자( `'?'`, `'&'`, `'='`중첩된 요청 내에서 는 HTTP 인코딩이 아니어야 합니다. 사실상, 임베드된 요청들은 외부(임베딩) 요청과 동일하게 인코딩되어야 한다.

중첩 요청에서 지정할 때 다음 이미지 렌더링 명령은 무시됩니다.

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

또한 무시됩니다. `attribute::MaxPix` 및 `attribute::DefaultPix` 중첩된 렌더링 요청에 적용되는 재질 카탈로그의 수입니다.

중첩된 IR 요청의 이미지 결과는 다음을 포함하여 선택적으로 캐시될 수 있습니다. `cache=on`. 기본적으로 중간 데이터의 캐싱은 비활성화되어 있습니다. 적절한 기간 내에 중간 이미지를 다른 요청에서 재사용할 것으로 예상되는 경우에만 캐싱을 활성화해야 합니다. 표준 서버측 캐시 관리가 적용됩니다. 데이터는 무손실 형식으로 캐시됩니다.

## 포함된 FXG 렌더링 요청 {#section-c817e4b4f7da414ea5a51252ca7e120a}

FXG 그래픽 렌더러(예: [!DNL AGMServer])가 설치되고 이미지 제공에서 활성화되므로 FXG 요청을에서 지정하여 레이어 소스로 사용할 수 있습니다 `src=` (또는 `mask=`) 명령을 입력합니다. 다음 구문을 사용합니다.

`…&src=fxg( renderRequest)&…`

다음 `fxg` 토큰은 대/소문자를 구분합니다.

>[!NOTE]
>
>FXG 그래픽 렌더링은 Dynamic Media 호스팅 환경에서만 사용할 수 있으며 추가 라이선스가 필요할 수 있습니다. 자세한 내용은 Dynamic Media 기술 지원 센터에 문의하십시오.

*[!DNL renderRequest]* 는 HTTP 루트 경로를 제외한 일반적인 FXG 렌더링 요청입니다. ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>구분 기호 문자( `'(',')'`) 및 명령 구분 기호 문자( `'?'`, `'&'`, `'='`중첩된 요청 내에서 는 HTTP 인코딩이 아니어야 합니다. 사실상, 임베드된 요청들은 외부(임베딩) 요청과 동일하게 인코딩되어야 한다.

중첩 요청에서 지정할 때 다음 FXG 명령은 무시됩니다.

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## 외부 이미지 소스 {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

이미지 제공은 외부 HTTP 서버의 소스 이미지에 대한 액세스를 지원합니다.

>[!NOTE]
>
>원격 URL에 대해서는 HTTP 프로토콜만 지원됩니다.

에 대한 외부 URL을 지정하려면 `src=` 또는 `mask=` 외래 URL 또는 URL 조각은 괄호로 묶어 구분하십시오.

`…&src=( foreignUrl)&…`

중요 구분 기호 문자( `'(',')'`) 및 명령 구분 기호 문자( `'?'`, `'&'`, `'='`중첩된 요청 내에서 는 HTTP 인코딩이 아니어야 합니다. 사실상, 임베드된 요청들은 외부(임베딩) 요청과 동일하게 인코딩되어야 한다.

전체 절대 URL(다음의 경우) `attribute::AllowDirectUrls` 가 설정됨)이고, URL은 `attribute::RootUrl` 허용됩니다. 절대 URL이 포함되고 속성이 다음과 같은 경우 오류가 발생합니다. `AllowDirectUrls` 은 0이거나, 상대 URL이 지정된 경우 이고 `attribute::RootUrl` 은(는) 비어 있습니다.

요청 URL의 경로 구성 요소에 외부 URL을 직접 지정할 수는 없지만, 상대 경로를 절대 URL로 변환하는 전처리 규칙을 설정할 수 있습니다(아래 예 참조).

외부 이미지는 HTTP 응답에 포함된 캐싱 헤더에 따라 서버에 의해 캐시됩니다. 둘 다 `ETag` Last-Modified HTTP 응답 헤더가 없으면 응답이 캐시되지 않습니다. 이 경우 이미지 제공이 모든 액세스에서 이미지를 다시 가져오고 유효성을 다시 검사해야 하므로 동일한 외부 이미지에 대한 반복 액세스의 성능이 저하될 수 있습니다.

이 메커니즘은 구성 요소당 16비트가 있는 소스 이미지를 제외하고 이미지 변환 (IC) 유틸리티에서 지원하는 것과 동일한 이미지 파일 형식을 지원합니다.

>[!NOTE]
>
>이미지 제공은 외부 이미지를 처음 사용할 때 유효성 검사 유틸리티를 자동으로 실행하여 이미지가 유효하고 전송 중에 손상되지 않았는지 확인합니다. 이로 인해 첫 번째 액세스가 약간 지연될 수 있습니다. 최상의 성능을 위해서는 이러한 이미지의 크기를 제한하거나 잘 압축되는 이미지 파일 형식을 사용하는 것이 좋습니다.

## 제한 사항 {#section-fb68e3f0d40947feb94d7bf183b64929}

중첩/임베드된 요청으로 생성된 이미지의 크기는 일반적으로 자동으로 최적화됩니다. 중첩된 요청 이미지 캐싱이 활성화되면 중첩된 이미지의 정확한 크기를 지정하여 점진적인 성능 향상을 실현할 수 있으므로 캐시 항목을 재사용할 때 더 이상의 확장이 필요하지 않습니다.

중요 이미지 제공에서는 중첩 요청이나 포함된 요청의 이중 인코딩을 지원하지 않습니다. 중첩된 요청과 포함된 요청은 단순 요청과 마찬가지로 HTTP 인코딩이 적용되어야 합니다.

## 예제 {#section-d800cfc31abe46d2a964f8e7929231f1}

**캐싱을 사용한 계층화 템플릿:**

중첩을 사용하여 레이어 템플릿에 캐싱을 추가합니다. 제한된 수의 배경 이미지가 고도로 가변적인 텍스트로 오버레이됩니다. 초기 템플릿 문자열은 다음과 같습니다.

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

약간의 수정 사항으로 레이어 0 이미지의 크기를 미리 조정하고 지속적으로 캐시하여 서버 로드를 줄일 수 있습니다.

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Dynamic Media 이미지 렌더링에 대한 요청 포함**

에 저장된 템플릿 사용 [!DNL myCatalog/myTemplate]: Dynamic Media 이미지 렌더링을 사용하여 템플릿의 레이어2에 대한 이미지를 생성합니다.

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

중첩된 중괄호를 확인합니다. 이미지 렌더링 요청은 반복 가능한 텍스처를 검색하도록 이미지 서비스 제공에 대한 호출을 임베드합니다.

## 참조 {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [마스크=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [요청 전처리](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), 이미지 렌더링 참조, [템플릿](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [이미지 서비스 제공 유틸리티](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
