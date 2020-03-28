---
description: 이미지 렌더링은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 사전 처리 메커니즘을 지원합니다.
seo-description: 이미지 렌더링은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 사전 처리 메커니즘을 지원합니다.
seo-title: 규칙 세트 참조
solution: Experience Manager
title: 규칙 세트 참조
topic: Scene7 Image Serving - Image Rendering API
uuid: aeec7597-4d23-4cf8-8bdc-3a133152eadb
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 규칙 세트 참조{#rule-set-reference}

이미지 렌더링은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 사전 처리 메커니즘을 지원합니다.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

사전 처리 규칙(*규칙 세트*)의 컬렉션은 재료 카탈로그 또는 기본 카탈로그에 첨부할 수 있습니다. 기본 카탈로그의 규칙은 요청이 특정 자재 카탈로그를 첨부하지 않는 경우에만 적용됩니다.

요청 사전 처리 규칙은 경로 조작, 명령 추가, 명령 값 변경, 템플릿 또는 매크로 적용 등 서버의 요청 파서에서 처리하기 전에 요청의 경로와 쿼리 부분을 수정할 수 있습니다. 규칙을 사용하여 일부 카탈로그 속성을 구성하고 재정의할 수 있을 뿐만 아니라 특정 클라이언트 IP 주소로 서비스를 제한할 수도 있습니다.

규칙 세트는 XML 문서 파일로 저장됩니다. 규칙 세트 파일의 상대 경로 또는 절대 경로는 에 지정해야 합니다 `attribute::RuleSetFile`.

## 일반 구조 {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
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
   </rule>
</ruleset>
```

실제 규칙이 정의되지 않은 경우에도 `<?xml>`유효한 규칙 세트 XML 파일에서 `<!DOCTYPE>` 및 `<ruleset>` 요소는 항상 필요합니다.

요소 수를 포함하는 `<ruleset>` 하나의 `<rule>` 요소가 허용됩니다.

사전 처리 규칙 파일의 내용은 대/소문자를 구분합니다.

## URL 사전 처리 {#section-737a38d1b8c746f995e64fa6cfbcec87}

다른 처리 전에 들어오는 HTTP 요청이 부분적으로 구문 분석되어 적용할 재료 카탈로그를 결정합니다. 카탈로그가 식별되면 선택한 카탈로그(또는 특정 카탈로그를 식별하지 않은 경우 기본 카탈로그)에 대한 규칙 세트가 적용됩니다.

요소의 `<rule>` 내용과 일치하기 위해 지정된 순서대로 `<expression>` 요소가 검색됩니다( *`expression`*).

a `<rule>` 가 일치하면 선택 사항이 *`substitution`* 적용되고 수정된 요청 문자열이 정상적인 처리를 위해 서버의 요청 파서에 전달됩니다.

끝 부분에 도달할 때 `<ruleset>` 일치하는 항목이 없으면 요청이 수정 없이 구문 분석기로 전달됩니다.

## OnMatch 속성 {#section-7a8ad3597780486985af5e9a3b1c7b56}

기본 동작은 요소의 `OnMatch` 속성을 사용하여 수정할 수 `<rule>` 있습니다. `OnMatch` 은 `break` (기본값), `continue`또는 `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>요소 및 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>일치 시 동작 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>이 규칙에 대한 대체가 적용된 후 규칙 처리가 즉시 종료됩니다. 기본값. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>대체가 적용되고 다음 규칙이 계속 처리됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>규칙 처리가 즉시 종료되고 "요청이 거부됨" 응답 상태가 클라이언트에 반환됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 카탈로그 속성 재정의 {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 요소는 규칙이 성공적으로 일치하고 설정될 때 해당 카탈로그 속성을 무시하는 속성을 선택적으로 정의할 `OnMatch="break"` 수 있습니다. 설정된 경우 속성이 적용되지 `OnMatch="continue"` 않습니다. 규칙으로 제어할 수 있는 속성 목록은 의 설명을 `<rule>` 참조하십시오.

## 정규 표현식 {#section-4d326507b52544b0960a9a5f303e3fe6}

간단한 문자열 일치는 매우 기본적인 응용 프로그램에서 작동하지만 대부분의 경우 정규 표현식이 필요합니다. 정규 표현식은 업계 표준이지만 특정 구현은 인스턴스마다 다릅니다.

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 는 이미지 제공에서 사용되는 특정 정규 표현식 구현에 대해 설명합니다.

## 캡처된 하위 문자열 {#section-8057cd65d48949ffb6a50e929bd3688b}

복잡한 URL 수정을 용이하게 하기 위해 하위 문자열을 괄호(...)로 묶어 식에서 캡처할 수 있습니다. 캡처한 하위 문자열은 선행 괄호 위치에 따라 1부터 순차적으로 번호가 매겨집니다. 캡처된 하위 문자열은 대체에 삽입될 수 있습니다. *`$n`*&#x200B;여기서 *`n`* 는 캡처된 하위 문자열의 시퀀스 번호입니다.

## 규칙 세트 파일 관리 {#section-e8ce976b56404c009496426fd334d23d}

하나의 규칙 세트 파일을 카탈로그 속성과 함께 각 재료 카탈로그에 첨부할 수 `attribute::RuleSetFile`있습니다. 언제든지 규칙 세트 파일을 편집할 수 있지만 이미지 서버는 연결된 재료 카탈로그가 다시 로드될 때만 변경 사항을 인식합니다. 이 문제는 Platform Server가 시작되거나 다시 시작될 때와 파일 접미사가 있는 기본 카탈로그 파일이 수정되거나 &#39;터치됨&#39;(파일 날짜 변경)이 될 때마다 발생합니다. [!DNL .ini]

## 예제 {#section-c4142a41f5cd4ff799a72fbc130c3700}

규칙 세트 예는 이미지 제공 설명서의 이미지 카탈로그 참조에서 해당 섹션에 제공됩니다.

## 참조 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
