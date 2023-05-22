---
title: setLocalizedText
description: 회전판 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8ffb8960-187a-43ab-8081-7dfd95d4c75d
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# setLocalizedText{#setlocalizedtexts}

회전판 뷰어에 대한 JavaScript API 참조.

` setLocalizedTexts( *`localizationInfo`*)`

하나 이상의 로케일에 대한 지역화 SYMBOL 값을 설정합니다. 이 매개 변수는 다음 전에 호출해야 합니다. `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> 오브젝트</span>현지화 데이터가 있는 } JSON 개체. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> 사용자 인터페이스 요소의 현지화</a> 추가 정보. </p> <p>다음 항목도 참조하십시오. <i>Viewer SDK 사용 안내서</i> 객체의 컨텐트에 대한 자세한 내용은 예제를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

참조: [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```
