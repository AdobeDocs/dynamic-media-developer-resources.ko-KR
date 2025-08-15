---
description: 이미지 렌더링은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 전처리 메커니즘을 지원합니다.
solution: Experience Manager
title: 규칙 세트 참조
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# 규칙 세트 참조{#rule-set-reference}

이미지 렌더링은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 전처리 메커니즘을 지원합니다.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

사전 처리 규칙 컬렉션(*규칙 집합*)을 재질 카탈로그 또는 기본 카탈로그에 첨부할 수 있습니다. 기본 카탈로그의 규칙은 요청이 특정 재질 카탈로그를 첨부하지 않는 경우에만 적용됩니다.

요청 전처리 규칙은 서버의 요청 파서에서 처리하기 전에 경로 조작, 명령 추가, 명령 값 변경, 템플릿 또는 매크로 적용 등 요청의 경로와 쿼리 부분을 수정할 수 있습니다. 규칙을 사용하여 일부 카탈로그 속성을 구성 및 재정의하고 서비스를 특정 클라이언트 IP 주소로 제한할 수도 있습니다.

규칙 세트는 XML 문서 파일로 저장됩니다. 규칙 집합 파일의 상대 또는 절대 경로를 `attribute::RuleSetFile`에 지정해야 합니다.

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

실제 규칙이 정의되지 않은 경우에도 `<?xml>`, `<!DOCTYPE>` 및 `<ruleset>` 요소는 항상 올바른 규칙 집합 XML 파일에 필요합니다.

`<ruleset>`개 요소를 포함하는 하나의 `<rule>` 요소가 허용됩니다.

전처리 규칙 파일의 내용은 대/소문자를 구분합니다.

## URL 사전 처리 {#section-737a38d1b8c746f995e64fa6cfbcec87}

다른 처리 전에 들어오는 HTTP 요청을 부분적으로 구문 분석하여 어떤 재질 카탈로그를 적용해야 하는지 결정합니다. 카탈로그가 식별되면 선택한 카탈로그(또는 특정 카탈로그가 식별되지 않은 경우 기본 카탈로그)에 대한 규칙 세트가 적용됩니다.

`<rule>` 요소는 `<expression>` 요소(*`expression`*)의 내용과 일치하는 항목을 위해 지정된 순서대로 검색됩니다.

`<rule>`이(가) 일치하면 선택적 *`substitution`*&#x200B;이(가) 적용되고 정상적인 처리를 위해 수정된 요청 문자열이 서버의 요청 파서로 전달됩니다.

`<ruleset>`의 끝에 도달했을 때 일치하는 항목이 없으면 수정 없이 파서에 요청이 전달됩니다.

## OnMatch 특성 {#section-7a8ad3597780486985af5e9a3b1c7b56}

`OnMatch` 요소의 `<rule>` 특성을 사용하여 기본 동작을 수정할 수 있습니다. `OnMatch`은(는) `break`(기본값), `continue` 또는 `error.`(으)로 설정될 수 있습니다.

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>요소 및 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>일치 발생 시 비헤이비어 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>규칙 처리는 이 규칙에 대한 대체가 적용된 직후에 종료됩니다. 기본값. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>대체가 적용되며 처리는 다음 규칙을 사용하여 계속됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>규칙 처리가 즉시 종료되고 "요청 거부됨" 응답 상태가 클라이언트에 반환됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 카탈로그 속성 재정의 {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 요소는 규칙이 성공적으로 일치하고 `OnMatch="break"`이(가) 설정된 경우 해당 카탈로그 특성을 재정의하는 특성을 선택적으로 정의할 수 있습니다. `OnMatch="continue"`이(가) 설정된 경우 특성이 적용되지 않습니다. 규칙으로 제어할 수 있는 특성 목록은 `<rule>`의 설명을 참조하십시오.

## 정규 표현식 {#section-4d326507b52544b0960a9a5f303e3fe6}

간단한 문자열 일치는 매우 기본적인 응용 프로그램에 대해 작동하지만 대부분의 경우 정규 표현식이 필요합니다. 정규 표현식은 업계 표준이지만 특정 구현은 인스턴스마다 다릅니다.

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)에서는 이미지 제공에 사용되는 특정 정규 표현식 구현을 설명합니다.

## 캡처된 하위 문자열 {#section-8057cd65d48949ffb6a50e929bd3688b}

복잡한 URL 수정을 용이하게 하기 위해 하위 문자열을 괄호(...)로 묶어 표현식에서 하위 문자열을 캡처할 수 있습니다. 캡처된 하위 문자열은 선행 괄호의 위치에 따라 1부터 순차적으로 번호가 매겨진다. 캡처된 하위 문자열은 *`$n`*&#x200B;을(를) 사용하여 대체에 삽입할 수 있습니다. 여기서 *`n`*&#x200B;은(는) 캡처된 하위 문자열의 시퀀스 번호입니다.

## 규칙 세트 파일 관리 {#section-e8ce976b56404c009496426fd334d23d}

카탈로그 특성이 `attribute::RuleSetFile`인 각 재질 카탈로그에 하나의 규칙 집합 파일을 첨부할 수 있습니다. 언제든지 규칙 세트 파일을 편집할 수 있지만 이미지 서버는 연관된 재료 카탈로그가 다시 로드될 때만 변경 사항을 인식합니다. 이 문제는 [!DNL Platform Server]을(를) 시작하거나 다시 시작할 때 및 기본 카탈로그 파일([!DNL .ini] 파일 접미사 포함)을 수정하거나 &#39;터치&#39;(파일 날짜를 변경하기 위해)할 때마다 발생합니다.

## 예제 {#section-c4142a41f5cd4ff799a72fbc130c3700}

규칙 세트 예는 이미지 서비스 제공 설명서의 이미지 카탈로그 참조의 해당 섹션에 제공됩니다.

## 참조 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[패키지 java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
