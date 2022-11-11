---
description: 이미지 제공 기능은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 사전 처리 메커니즘을 지원합니다.
solution: Experience Manager
title: 규칙 세트 참조
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# 규칙 세트 참조{#rule-set-reference}

이미지 제공 기능은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 사전 처리 메커니즘을 지원합니다.

사전 처리 규칙 컬렉션(*규칙 세트*)를 이미지 카탈로그 또는 기본 카탈로그에 첨부할 수 있습니다. 기본 카탈로그의 규칙은 요청이 특정 주 이미지 카탈로그를 식별하지 않는 경우에만 적용됩니다.

요청 사전 처리 규칙은 요청에 의해 처리되기 전에 요청의 경로 및 쿼리 부분을 수정할 수 있습니다. [!DNL Platform Server]경로 조작, 명령 추가, 명령 값 변경, 템플릿 또는 매크로 적용 등 의 파서입니다. 규칙을 사용하여 요청 난독화, 워터마킹 등의 카탈로그 속성으로만 일반적으로 제어되고 특정 클라이언트 IP 주소로 서비스를 제한하는 특정 보안 기능을 구성하고 재정의할 수도 있습니다.

규칙 세트는 XML 문서 파일로 저장됩니다. 규칙 세트 파일의 상대 또는 절대 경로는 `attribute::RuleSetFile`.

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

다음 `<?xml>` 및 `<ruleset>` 실제 규칙이 정의되지 않은 경우에도 항상 유효한 규칙 세트 XML 파일에 요소가 필요합니다.

1개 `<ruleset>` 개수가 포함된 요소 `<rule>` 요소가 허용됩니다.

사전 처리 규칙 파일의 내용은 대/소문자를 구분합니다.

## 규칙 세트 유효성 검사 {#section-d8d101a0b4d74580835e37d128d05567}

의 사본 [!DNL RuleSet.xsd] 은 카탈로그 폴더에 제공되며 규칙 세트 파일에 등록하기 전에 규칙 세트 파일의 유효성을 검사하는 데 사용해야 합니다 [!DNL catalog.ini] 파일. Image Serving은 [!DNL RuleSet.xsd] 유효성 검사

## URL 사전 처리 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

다른 처리 전에 들어오는 HTTP 요청을 부분적으로 구문 분석하여 어떤 이미지 카탈로그를 적용해야 하는지 결정합니다. 카탈로그가 식별되면 선택한 카탈로그(또는 특정 카탈로그가 식별되지 않은 경우 기본 카탈로그)에 대한 규칙 세트가 적용됩니다.

다음 `<rule>` 요소의 콘텐츠와 일치하기 위해 지정한 순서대로 요소가 검색됩니다 `<expression>` 요소( *`expression`*).

다음과 같은 경우 `<rule>` 일치하고 선택 사항입니다 *`substitution`* 가 적용되고 수정된 요청 문자열이 정상적인 처리를 위해 서버의 요청 파서에 전달됩니다.

의 끝에 일치하는 항목이 없으면 `<ruleset>` 이(가) 도달하면 요청이 수정 없이 파서에 전달됩니다.

## OnMatch 속성 {#section-ed952fa55d99422db0ee68a2b9d395d3}

기본 동작은 `OnMatch` 의 속성 `<rule>` 요소를 생성하지 않습니다. `OnMatch` 는 로 설정되었을 수 있습니다. `break` (기본값), `continue`, 또는 `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>요소 및 속성</b> </th> 
   <th class="entry"> <b>일치하는 경우 동작</b> </th> 
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
   <td> <p>규칙 처리가 즉시 종료되고 "요청 거부" 응답 상태가 클라이언트에 반환됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 카탈로그 속성 재정의 {#section-3f1e33a65c5346d1b4a69958c61432f3}

다음 `rule` 요소가 선택적으로 규칙이 성공적으로 일치할 때 해당 카탈로그 속성을 재정의하는 속성을 정의할 수 있습니다. 일치하는 규칙이 여러 개 설정되어 있으면 마지막 규칙이 우선합니다. 자세한 내용은 [규칙](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) 규칙으로 제어할 수 있는 속성 목록에 대한 요소입니다.

## 정규 표현식 {#section-3f77bb9a265147b38c645f63ab1bad8b}

간단한 문자열 일치 기능은 매우 기본적인 응용 프로그램에 대해 작동하지만 대부분의 경우 정규 표현식이 필요합니다. 정규 표현식은 업계 표준이지만 특정 구현은 인스턴스에 따라 다릅니다.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 이미지 제공 기능에서 사용하는 특정 정규 표현식 구현에 대해 설명합니다.

## 캡처된 하위 문자열 {#section-066e659406d5403599cd26ae35e80d68}

복잡한 URL을 쉽게 수정할 수 있도록 하위 문자열을 괄호(..)로 묶어서 표현식에서 캡처할 수 있습니다. 캡처된 부분 문자열은 선행 괄호의 위치에 따라 순차적으로 1로 번호가 매겨집니다. 캡처된 부분 문자열은 ` $ *`n`*`, 위치 *`n`* 는 캡처된 하위 문자열의 시퀀스 번호입니다.

## 규칙 세트 파일 관리 {#section-0598a608e4044bb4805fe93ceebe10a9}

카탈로그 속성을 사용하여 각 이미지 카탈로그에 하나의 규칙 세트 파일을 첨부할 수 있습니다 `attribute::RuleSetFile`. 언제든지 규칙 세트 파일을 편집할 수 있지만 이미지 서버는 연결된 이미지 카탈로그가 다시 로드될 때만 변경 내용을 인식합니다. 이러한 다시 로딩은 플랫폼 서버가 시작되거나 다시 시작될 때와 기본 카탈로그 파일이 [!DNL .ini] 파일 접미사, 수정 또는 터치됨 등을 사용하여 파일 날짜를 변경합니다.

## 예제 {#section-aa769437d967459299b83a4bf34fe924}

**예 A.** 이미지 이름에 &quot; 접미사가 있는 경우 이미지 품질 설정을 늘리는 규칙을 정의합니다. [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

규칙 식은 대/소문자를 구분하지 않는 &quot; 일치를 지정합니다. [!DNL _hg]&quot;를 입력합니다. 접미사는 이미지 품질 설정을 변경하는 지정된 쿼리 문자열로 대체됩니다. 다음 사항에 유의하십시오. `?` 대체 문자열의 문자는 정규 표현식에서 특수 문자이므로 이스케이프 처리됩니다.

>[!NOTE]
>
>앰퍼샌드 문자의 필수 인코딩입니다. 또는 대체 문자열을 CDATA 블록으로 묶을 수 있습니다.

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**예 B.** 특정 웹 응용 프로그램에서 쿼리 문자열을 허용하지 않습니다. 후행 경로 요소를 해석하는 규칙을 정의합니다 `small`, `medium`, 또는 `large` 템플릿에 추가합니다. 나머지 경로를 이미지 이름으로 사용합니다. 예, `myCat/myImage/small` 이 `myCat/smallTemplate?src=myCat/myImage`.

부분 문자열을 사용하여 요청을 재구성할 수 있습니다.

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 참조 {#section-9b748e7c5cff4759a70f96657bd43352}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
