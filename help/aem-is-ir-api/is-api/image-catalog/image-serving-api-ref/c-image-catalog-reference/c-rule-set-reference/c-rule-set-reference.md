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
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 0%

---


# 규칙 세트 참조{#rule-set-reference}

이미지 제공은 정규 표현식 일치 및 대체 규칙을 기반으로 하는 간단한 요청 사전 처리 메커니즘을 지원합니다.

사전 처리 규칙 컬렉션(*규칙 세트*)은 이미지 카탈로그 또는 기본 카탈로그에 첨부할 수 있습니다. 기본 카탈로그의 규칙은 요청이 특정 기본 이미지 카탈로그를 식별하지 않는 경우에만 적용됩니다.

요청 사전 처리 규칙은 경로 조작, 명령 추가, 명령 값 변경, 템플릿 또는 매크로 적용 등 플랫폼 서버의 파서에서 처리하기 전에 요청의 경로와 쿼리 부분을 수정할 수 있습니다. 또한 규칙을 사용하여 요청 난독화, 워터마크 등의 카탈로그 속성으로만 정상적으로 제어되는 특정 보안 기능을 구성 및 재정의하고 특정 클라이언트 IP 주소로 서비스를 제한하는 데 사용할 수 있습니다.

규칙 세트는 XML 문서 파일로 저장됩니다. 규칙 세트 파일의 상대 또는 절대 경로는 `attribute::RuleSetFile`에 지정해야 합니다.

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

실제 규칙을 정의하지 않더라도 유효한 규칙 세트 XML 파일에서 `<?xml>` 및 `<ruleset>` 요소는 항상 필요합니다.

`<rule>` 요소 수를 포함하는 `<ruleset>` 요소 하나를 사용할 수 있습니다.

처리 규칙 파일의 내용은 대/소문자를 구분합니다.

## 규칙 집합 유효성 검사 {#section-d8d101a0b4d74580835e37d128d05567}

[!DNL RuleSet.xsd]의 사본이 카탈로그 폴더에 제공되므로 규칙 세트 파일을 [!DNL catalog.ini] 파일에 등록하기 전에 규칙 세트 파일의 유효성을 검사하는 데 사용해야 합니다. 이미지 제공 기능에서는 유효성 검사를 위해 [!DNL RuleSet.xsd]의 내부 복사본을 사용합니다.

## URL 사전 처리 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

다른 처리 전에 들어오는 HTTP 요청을 부분적으로 구문 분석하여 어떤 이미지 카탈로그를 적용할지 결정합니다. 카탈로그를 식별하면 선택한 카탈로그에 대한 규칙 세트(또는 특정 카탈로그를 식별하지 못한 경우 기본 카탈로그)가 적용됩니다.

`<rule>` 요소는 `<expression>` 요소의 내용( *`expression`*)과 일치하기 위해 지정된 순서로 검색됩니다.

`<rule>`이(가) 일치하면 선택적 *`substitution`*&#x200B;이 적용되고 수정된 요청 문자열이 서버의 요청 구문 분석기에 전달되어 정상적인 처리가 수행됩니다.

`<ruleset>`의 끝에 도달할 때 일치하는 항목이 없으면 요청이 수정 없이 파서로 전달됩니다.

## OnMatch 특성 {#section-ed952fa55d99422db0ee68a2b9d395d3}

기본 동작은 `<rule>` 요소의 `OnMatch` 특성으로 수정할 수 있습니다. `OnMatch` 은  `break` (기본값),  `continue`또는  `error`로 설정될 수 있습니다.

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
   <td> <p>이 규칙에 대한 대체가 적용된 즉시 규칙 처리가 종료됩니다. 기본값. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>대체를 적용하고 다음 규칙에 따라 처리가 계속됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>규칙 처리가 즉시 종료되고 "요청이 거부됨" 응답 상태가 클라이언트에 반환됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 카탈로그 특성 재정의 중 {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` 규칙이 성공적으로 일치할 때 해당 카탈로그 속성을 무시하는 속성을 선택적으로 정의할 수 있습니다. 일치하는 여러 규칙이 동일한 속성을 설정하는 경우 마지막 규칙이 우선합니다. 규칙으로 제어할 수 있는 특성 목록은 ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` 요소의 설명을 참조하십시오.

## 정규 표현식 {#section-3f77bb9a265147b38c645f63ab1bad8b}

간단한 문자열 일치는 매우 기본적인 응용 프로그램에 대해 작동하지만 대부분의 경우 일반 표현식이 필요합니다. 일반 표현식은 업계 표준이지만 특정 구현은 인스턴스마다 다릅니다.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 이미지 제공에서 사용하는 특정 정규식 구현을 설명합니다.

## 캡처한 하위 문자열 {#section-066e659406d5403599cd26ae35e80d68}

복잡한 URL 수정을 용이하게 하기 위해 부분 문자열을 괄호(..)로 묶어서 표현식에 캡처할 수 있습니다. 캡처한 하위 문자열은 선행 괄호 위치에 따라 1부터 순차적으로 번호가 매겨집니다. 캡처한 하위 문자열을 ` $ *`n`*`을 사용하여 대체 항목에 삽입할 수 있습니다. 여기서 *`n`*&#x200B;는 캡처된 하위 문자열의 시퀀스 번호입니다.

## 규칙 세트 파일 관리 {#section-0598a608e4044bb4805fe93ceebe10a9}

하나의 규칙 세트 파일을 카탈로그 속성 `attribute::RuleSetFile`과 함께 각 이미지 카탈로그에 첨부할 수 있습니다. 언제든지 규칙 세트 파일을 편집할 수 있지만 이미지 서버는 연결된 이미지 카탈로그를 다시 로드할 때만 변경 사항을 인식합니다. 이러한 다시 로드는 플랫폼 서버를 시작하거나 다시 시작할 때와 [!DNL .ini] 파일 접미어를 가진 기본 카탈로그 파일이 수정되거나 &quot;손질&quot;될 때마다 파일 날짜를 변경합니다.

## 예제 {#section-aa769437d967459299b83a4bf34fe924}

**예 A.** 이미지 이름에 접미사 &quot;&quot;가 있는 경우 이미지 품질 설정을 늘리는 규칙을  [!DNL _hg]정의합니다.

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

규칙 표현식은 URL 문자열 끝에 있는 &quot; [!DNL _hg]&quot;의 대/소문자를 구분하지 않는 일치를 지정합니다. 접미어는 이미지 품질 설정을 변경하는 지정된 쿼리 문자열로 대체됩니다. 일반 표현식의 특수 문자이므로 대체 문자열의 `?` 문자는 이스케이프됩니다.

>[!NOTE]
>
>앰퍼샌드 문자에 필요한 인코딩입니다. 또는 대체 문자열을 CDATA 블록으로 묶을 수도 있습니다.

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**예 B.** 특정 웹 응용 프로그램은 쿼리 문자열을 허용하지 않습니다. 경로의 나머지를 이미지 이름으로 사용하여 후행 경로 요소 `small`, `medium` 또는 `large`를 템플릿으로 변환하는 규칙을 정의합니다. 예를 들어 `myCat/myImage/small`은(는) `myCat/smallTemplate?src=myCat/myImage`로 변환됩니다.

아래 문자열을 사용하여 요청을 재구성할 수 있습니다.

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 참조 {#section-9b748e7c5cff4759a70f96657bd43352}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
