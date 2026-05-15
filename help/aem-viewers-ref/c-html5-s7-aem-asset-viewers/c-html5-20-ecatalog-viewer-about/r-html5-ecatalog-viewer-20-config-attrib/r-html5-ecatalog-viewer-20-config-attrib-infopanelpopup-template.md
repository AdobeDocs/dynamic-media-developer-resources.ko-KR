---
title: InfoPanelPopup.template
description: InfoPanelPopup.template
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
TQID: 'https://experienceleague.adobe.com/e-j3Y9zymMOwlwNcz6Ouh0Asn1m5u-lx5zoRfUORN2U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 196
ht-degree: 2%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`템플릿`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> 템플릿</span></span> </p> </td> 
   <td> <p>정보 서버에서 반환된 데이터가 병합되는 컨텐츠 템플릿입니다. </p> <p>컨텐트 템플릿은 이 DTD 다음에 나오는 XML입니다. </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;&lbrack;
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      &rbrack;&gt;</code> </p> <p>콘텐츠 템플릿의 실제 구문은 다음과 같습니다. </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&rbrack;&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>즉, 템플릿은 선택적 기본 <span class="codeph"> &lt;var&gt;</span> 요소를 포함할 수 있는 <span class="codeph"> &lt;info&gt;</span> 요소로 시작해야 합니다. 템플릿 콘텐츠 자체 <span class="codeph"> TEMPLATE_CONTENT</span>이(가) HTML 텍스트입니다. 또한 콘텐츠 템플릿에는 정보 서버가 반환하는 변수 값이나 기본 변수 값으로 대체되는 <span class="codeph"> $</span>자로 둘러싸인 변수 이름이 포함될 수 있습니다. </p> <p>템플릿에 정의된 기본 변수는 전역(롤오버 특성이 설정되지 않은 경우) 또는 특정 롤오버 키(롤오버 특성이 있는 경우)일 수 있습니다. </p> <p>키를 롤오버하는 데 특정한 템플릿 처리 변수는 전역 변수보다 우선합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>정보 패널 팝업을 구성하면 정보 패널에 전달된 HTML 코드 및 JavaScript 코드가 클라이언트의 컴퓨터에서 실행됩니다. 따라서 이러한 HTML 코드 및 JavaScript 코드가 안전한지 확인하십시오.

## 속성 {#section-6dd7785357d740d095fa9f7fd0f67da4}

선택적.

## 기본값 {#section-cd5db06d08aa4de49e37d6c938b41570}

없음.

## 예 {#section-16d184665c484964af9a22f79ff3f840}

정보 서버 응답이 제품 이름을 변수 `$1$`(으)로 반환하고 제품 이미지 URL이 변수 `$2$`(으)로 반환된다고 가정합니다.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
