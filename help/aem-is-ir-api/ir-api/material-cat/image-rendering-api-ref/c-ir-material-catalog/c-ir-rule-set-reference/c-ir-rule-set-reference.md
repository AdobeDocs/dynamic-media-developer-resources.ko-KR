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
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---


# 규칙 세트 참조{#rule-set-reference}

이미지 렌더링은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 사전 처리 메커니즘을 지원합니다.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

사전 처리 규칙 컬렉션(*규칙 세트*)은 재료 카탈로그 또는 기본 카탈로그에 첨부할 수 있습니다. 기본 카탈로그의 규칙은 요청이 특정 자료 카탈로그를 첨부하지 않는 경우에만 적용됩니다.

요청 사전 처리 규칙은 경로 조작, 명령 추가, 명령 값 변경, 템플릿 또는 매크로 적용 등 서버의 요청 파서에서 처리하기 전에 요청의 경로와 쿼리 부분을 수정할 수 있습니다. 규칙을 사용하여 일부 카탈로그 속성을 구성하고 재정의할 수 있을 뿐만 아니라 특정 클라이언트 IP 주소로 서비스를 제한하는 데에도 사용할 수 있습니다.

규칙 세트는 XML 문서 파일로 저장됩니다. 규칙 세트 파일의 상대 또는 절대 경로는 `attribute::RuleSetFile`에 지정해야 합니다.

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

실제 규칙이 정의되지 않은 경우에도 항상 유효한 규칙 세트 XML 파일에서 `<?xml>`, `<!DOCTYPE>` 및 `<ruleset>` 요소가 필요합니다.

`<rule>` 요소 수를 포함하는 `<ruleset>` 요소 하나를 사용할 수 있습니다.

처리 규칙 파일의 내용은 대/소문자를 구분합니다.

## URL 사전 처리 {#section-737a38d1b8c746f995e64fa6cfbcec87}

다른 처리 전에 들어오는 HTTP 요청을 부분적으로 구문 분석하여 어떤 재료 카탈로그를 적용할지 결정합니다. 카탈로그를 식별하면 선택한 카탈로그에 대한 규칙 세트(또는 특정 카탈로그를 식별하지 못한 경우 기본 카탈로그)가 적용됩니다.

`<rule>` 요소는 `<expression>` 요소의 내용( *`expression`*)과 일치하기 위해 지정된 순서로 검색됩니다.

`<rule>`이(가) 일치하면 선택적 *`substitution`*&#x200B;이 적용되고 수정된 요청 문자열이 서버의 요청 구문 분석기에 전달되어 정상적인 처리가 수행됩니다.

`<ruleset>`의 끝에 도달할 때 일치하는 항목이 없으면 요청이 수정 없이 파서로 전달됩니다.

## OnMatch 특성 {#section-7a8ad3597780486985af5e9a3b1c7b56}

기본 동작은 `<rule>` 요소의 `OnMatch` 특성으로 수정할 수 있습니다. `OnMatch` 은  `break` (기본값),  `continue`또는  `error.`

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
   <td colname="col2"> <p>이 규칙에 대한 대체가 적용된 즉시 규칙 처리가 종료됩니다. 기본값. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>대체를 적용하고 다음 규칙에 따라 처리가 계속됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>규칙 처리가 즉시 종료되고 "요청이 거부됨" 응답 상태가 클라이언트에 반환됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 카탈로그 특성 재정의 중 {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 요소는 규칙이 성공적으로 일치하고 설정될 때 해당 카탈로그 속성을 재정의하는 속성 `OnMatch="break"` 을 선택적으로 정의할 수 있습니다. `OnMatch="continue"`이(가) 설정된 경우 속성이 적용되지 않습니다. 규칙으로 제어할 수 있는 특성 목록은 `<rule>`의 설명을 참조하십시오.

## 정규 표현식 {#section-4d326507b52544b0960a9a5f303e3fe6}

간단한 문자열 일치는 매우 기본적인 응용 프로그램에 대해 작동하지만 대부분의 경우 일반 표현식이 필요합니다. 일반 표현식은 업계 표준이지만 특정 구현은 인스턴스마다 다릅니다.

[패키지 java.util.](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) regexximplementation은 이미지 제공에서 사용하는 특정 정규식 구현을 설명합니다.

## 캡처한 하위 문자열 {#section-8057cd65d48949ffb6a50e929bd3688b}

복잡한 URL 수정을 용이하게 하기 위해 부분 문자열을 괄호(..)로 묶어서 표현식에 캡처할 수 있습니다. 캡처한 하위 문자열은 선행 괄호 위치에 따라 1부터 순차적으로 번호가 매겨집니다. 캡처한 하위 문자열을 *`$n`*&#x200B;을 사용하여 대체 항목에 삽입할 수 있습니다. 여기서 *`n`*&#x200B;은 캡처된 하위 문자열의 시퀀스 번호입니다.

## 규칙 세트 파일 관리 {#section-e8ce976b56404c009496426fd334d23d}

하나의 규칙 세트 파일을 카탈로그 속성 `attribute::RuleSetFile`과 함께 각 자료 카탈로그에 첨부할 수 있습니다. 언제든지 규칙 세트 파일을 편집할 수 있지만 이미지 서버는 연결된 자료 카탈로그를 다시 로드할 때만 변경 사항을 인식합니다. 이 문제는 Platform Server가 시작되거나 다시 시작될 때와 [!DNL .ini] 파일 접미어가 있는 기본 카탈로그 파일이 수정되거나 &#39;터치됨&#39;(파일 날짜를 변경하기 위해)이 될 때마다 발생합니다.

## 예제 {#section-c4142a41f5cd4ff799a72fbc130c3700}

규칙 세트 예는 이미지 제공 설명서의 이미지 카탈로그 참조에서 해당 섹션에 제공됩니다.

## 참조 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
