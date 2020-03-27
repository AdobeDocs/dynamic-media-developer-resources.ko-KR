---
description: 이미지 제공은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 사전 처리 메커니즘을 지원합니다.
seo-description: 이미지 제공은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 사전 처리 메커니즘을 지원합니다.
seo-title: 규칙 세트 참조
solution: Experience Manager
title: 규칙 세트 참조
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# 규칙 세트 참조{#rule-set-reference}

이미지 제공은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 사전 처리 메커니즘을 지원합니다.

사전 처리 규칙(*규칙 세트*)의 컬렉션은 이미지 카탈로그 또는 기본 카탈로그에 첨부할 수 있습니다. 기본 카탈로그의 규칙은 요청이 특정 기본 이미지 카탈로그를 식별하지 않는 경우에만 적용됩니다.

요청 사전 처리 규칙은 경로 조작, 명령 추가, 명령 값 변경, 템플릿 또는 매크로 적용 등 Platform Server의 파서에서 처리하기 전에 요청의 경로와 쿼리 부분을 수정할 수 있습니다. 또한 규칙을 사용하여 요청 난독화, 워터마킹, 특정 클라이언트 IP 주소로 서비스를 제한하는 등 일반적으로 카탈로그 속성으로만 제어되는 특정 보안 기능을 구성하고 재정의할 수도 있습니다.

규칙 세트는 XML 문서 파일로 저장됩니다. 규칙 세트 파일의 상대 경로 또는 절대 경로는 에 지정해야 합니다 `attribute::RuleSetFile`.

## 일반 구조 {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

실제 규칙이 정의되지 않은 경우에도 `<?xml>` 및 `<ruleset>` 요소는 항상 유효한 규칙 세트 XML 파일에서 필요합니다.

요소 수를 포함하는 `<ruleset>` 하나의 `<rule>` 요소가 허용됩니다.

사전 처리 규칙 파일의 내용은 대/소문자를 구분합니다.

## 규칙 세트 유효성 검사 {#section-d8d101a0b4d74580835e37d128d05567}

의 사본은 카탈로그 폴더에 [!DNL RuleSet.xsd] 제공되며, 규칙 세트 파일을 [!DNL catalog.ini] 파일에 등록하기 전에 유효성을 검사하는 데 사용해야 합니다. 이미지 제공에서는 유효성 검사를 위해 내부 복사본을 [!DNL RuleSet.xsd] 사용합니다.

## URL 사전 처리 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

다른 처리 전에 들어오는 HTTP 요청이 부분적으로 구문 분석되어 적용할 이미지 카탈로그를 결정합니다. 카탈로그가 식별되면 선택한 카탈로그(또는 특정 카탈로그를 식별하지 않은 경우 기본 카탈로그)에 대한 규칙 세트가 적용됩니다.

요소의 `<rule>` 내용과 일치하기 위해 지정된 순서대로 `<expression>` 요소가 검색됩니다( *`expression`*).

a `<rule>` 가 일치하면 선택 사항이 *`substitution`* 적용되고 수정된 요청 문자열이 정상적인 처리를 위해 서버의 요청 파서에 전달됩니다.

끝 부분에 도달할 때 `<ruleset>` 일치하는 항목이 없으면 요청이 수정 없이 구문 분석기로 전달됩니다.

## OnMatch 속성 {#section-ed952fa55d99422db0ee68a2b9d395d3}

기본 동작은 요소의 `OnMatch` 속성을 사용하여 수정할 수 `<rule>` 있습니다. `OnMatch` 은 `break` (기본값), `continue`또는 `error`으로 설정될 수 있습니다.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>요소 및 속성</b> </th> 
   <th class="entry"> <b>일치 시 동작</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>이 규칙에 대한 대체가 적용된 후 규칙 처리가 즉시 종료됩니다. 기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>대체가 적용되고 다음 규칙이 계속 처리됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>규칙 처리가 즉시 종료되고 "요청이 거부됨" 응답 상태가 클라이언트에 반환됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 카탈로그 속성 재정의 {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` 원할 경우 규칙이 성공적으로 일치할 때 해당 카탈로그 속성을 무시하는 속성을 정의할 수 있습니다. 일치하는 규칙이 여러 개 있으면 마지막 규칙이 우선합니다. 규칙으로 제어할 수 있는 속성 목록은 ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` 요소의 설명을 참조하십시오.

## 정규 표현식 {#section-3f77bb9a265147b38c645f63ab1bad8b}

간단한 문자열 일치는 매우 기본적인 응용 프로그램에서 작동하지만 대부분의 경우 정규 표현식이 필요합니다. 정규 표현식은 업계 표준이지만 특정 구현은 인스턴스마다 다릅니다.

[ [!DNL 패키지 java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 는 이미지 제공에서 사용되는 특정 정규 표현식 구현에 대해 설명합니다.

## 캡처된 하위 문자열 {#section-066e659406d5403599cd26ae35e80d68}

복잡한 URL 수정을 용이하게 하기 위해 하위 문자열을 괄호(...)로 묶어 식에서 캡처할 수 있습니다. 캡처한 하위 문자열은 선행 괄호 위치에 따라 1부터 순차적으로 번호가 매겨집니다. 캡처된 하위 문자열은 ` $ *`n을 사용하여`*`대체에서 삽입할 수 있습니다. 여기서 *`n`* 은 캡처된 하위 문자열의 시퀀스 번호입니다.

## 규칙 세트 파일 관리 {#section-0598a608e4044bb4805fe93ceebe10a9}

하나의 규칙 세트 파일을 카탈로그 속성과 함께 각 이미지 카탈로그에 첨부할 수 `attribute::RuleSetFile`있습니다. 언제든지 규칙 세트 파일을 편집할 수 있지만 이미지 서버는 연결된 이미지 카탈로그를 다시 로드할 때만 변경 사항을 인식합니다. 이러한 다시 로드는 플랫폼 서버를 시작하거나 다시 시작할 때와 파일 접미사가 있는 기본 카탈로그 파일이 수정되거나 &quot;손질&quot;될 때마다 파일 날짜를 변경합니다. [!DNL .ini]

## 예제 {#section-aa769437d967459299b83a4bf34fe924}

**예 A.** 이미지 이름에 접미사 &quot; [!DNL _hg]&quot;가 있으면 이미지 품질 설정을 높이는 규칙을 정의합니다.

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

규칙 표현식은 URL 문자열 끝에 있는 &quot; [!DNL _hg]&quot;의 대/소문자를 구분하지 않는 일치를 지정합니다. 접미사가 이미지 품질 설정을 변경하는 지정된 쿼리 문자열로 바뀝니다. 일반 표현식의 특수 문자이므로 대체 문자열의 `?` 문자는 이스케이프됩니다.

>[!NOTE]
>
>앰퍼샌드 문자에 필요한 인코딩입니다. 또는 대체 문자열을 CDATA 블록으로 묶을 수 있습니다.

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**예 B.** 특정 웹 응용 프로그램은 쿼리 문자열을 허용하지 않습니다. 경로의 나머지를 이미지 이름으로 사용하여 후행 경로 요소 `small``medium`또는 `large` 템플릿으로 변환하는 규칙을 정의합니다. 예를 들어 `myCat/myImage/small` 으로 번역할 `myCat/smallTemplate?src=myCat/myImage`수 있습니다.

하위 문자열을 사용하여 요청을 재구성할 수 있습니다.

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 참조 {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
