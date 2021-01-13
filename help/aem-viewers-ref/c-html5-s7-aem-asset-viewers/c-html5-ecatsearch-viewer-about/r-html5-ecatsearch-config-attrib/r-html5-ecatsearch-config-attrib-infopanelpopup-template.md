---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
topic: Dynamic media
uuid: a7b49f82-9a8b-45f8-b933-9880659770de
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`템플릿`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> 템플릿</span></span> </p> </td> 
   <td> <p>정보 서버에서 반환된 데이터가 병합되는 콘텐츠 템플릿입니다. </p> <p>컨텐츠 템플릿은 이 DTD 다음에 나오는 XML입니다. </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>컨텐츠 템플릿의 실제 구문은 다음과 같습니다. </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>즉, 템플릿은 선택적 기본 <span class="codeph"> &lt;var&gt;</span> 요소를 포함할 수 있는 <span class="codeph"> &lt;info&gt;</span> 요소로 시작해야 합니다. 템플릿 내용 자체인 <span class="codeph"> TEMPLATE_CONTENT</span>은(는) HTML 텍스트입니다. 또한 컨텐트 템플릿에는 <span class="codeph"> $</span> 문자로 둘러싸인 변수 이름이 포함될 수 있습니다. 이러한 문자는 정보 서버가 반환하는 변수 값 또는 기본 값으로 대체됩니다. </p> <p>템플릿에 정의된 기본 변수는 global(rollover 속성이 설정되지 않은 경우) 또는 특정 롤오버 키(rollover 속성이 있는 경우)에만 적용될 수 있습니다. </p> <p>키보다 롤오버하는 특정 템플릿 처리 변수는 글로벌 변수보다 우선합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>정보 패널 팝업을 구성할 때 정보 패널에 전달되는 HTML 코드 및 JavaScript 코드는 클라이언트의 컴퓨터에서 실행됩니다. 따라서 이러한 HTML 코드와 JavaScript 코드가 안전한지 확인하십시오.

## 속성 {#section-6dd7785357d740d095fa9f7fd0f67da4}

선택 사항입니다.

## 기본값 {#section-cd5db06d08aa4de49e37d6c938b41570}

없음.

## 예 {#section-16d184665c484964af9a22f79ff3f840}

정보 서버 응답이 제품 이름을 `$1$` 변수로 반환하고 제품 이미지 URL이 `$2$` 변수로 반환된다고 가정할 때

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
