---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 3%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`템플릿`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> 템플릿</span></span> </p> </td> 
   <td> <p>정보 서버에서 반환된 데이터가 병합되는 콘텐츠 템플릿입니다. </p> <p>컨텐트 템플릿은 이 DTD에 따른 XML입니다. </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>컨텐츠 템플릿의 실제 구문은 다음과 같습니다. </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>즉, 템플릿은 <span class="codeph"> &lt;info&gt;</span> 요소(선택적 기본값 <span class="codeph"> &lt;var&gt;</span> 요소)로 시작해야 합니다. 템플릿 컨텐츠 자체, <span class="codeph"> TEMPLATE_CONTENT</span>는 HTML 텍스트입니다. 또한 콘텐츠 템플릿에는 <span class="codeph"> $</span> 문자로 둘러싸인 변수 이름이 포함되어 있으며, 이 이름은 정보 서버가 반환하는 변수 값이나 기본 변수 값으로 대체됩니다. </p> <p>템플릿에 정의된 기본 변수는 전역(롤오버 속성이 설정되지 않은 경우) 또는 특정 롤오버 키(롤오버 속성이 있는 경우)에만 있을 수 있습니다. </p> <p>템플릿 처리 중 키 위에 롤오버되는 특정 변수가 전역 변수보다 우선합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>정보 패널 팝업을 구성할 때 정보 패널에 전달된 HTML 코드와 JavaScript 코드가 클라이언트의 컴퓨터에서 실행됩니다. 따라서 이러한 HTML 코드와 JavaScript 코드가 안전한지 확인하십시오.

## 속성 {#section-6dd7785357d740d095fa9f7fd0f67da4}

선택 사항입니다.

## 기본값 {#section-cd5db06d08aa4de49e37d6c938b41570}

없음.

## 예 {#section-16d184665c484964af9a22f79ff3f840}

정보 서버 응답이 제품 이름을 변수 `$1$`으로 반환하고 제품 이미지 URL이 변수 `$2$`로 반환된다고 가정할 때.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
