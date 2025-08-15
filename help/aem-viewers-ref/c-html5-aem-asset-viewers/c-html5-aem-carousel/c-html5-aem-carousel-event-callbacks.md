---
title: 이벤트 콜백
description: 이벤트 콜백
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: e87b2a84-735c-4412-a4dd-97b18474a1d2
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---

# 이벤트 콜백{#event-callbacks}

뷰어는 웹 페이지가 뷰어 초기화 프로세스 또는 런타임 동작을 추적하는 데 사용하는 JavaScript 이벤트 콜백을 지원합니다.

`handlers` 속성이 있는 이벤트 이름 및 해당 처리기 함수를 뷰어의 생성자에 있는 `config` JSON 개체로 전달하여 콜백 처리기를 할당합니다. 또는 `setHandlers()` API 메서드를 사용할 수 있습니다.

지원되는 뷰어 이벤트는 다음과 같습니다.

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>뷰어 이벤트 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete </span> </p> </td> 
   <td colname="col2"> <p>뷰어 초기화가 완료되고 모든 내부 구성 요소가 만들어지면 트리거되므로 <span class="codeph"> getComponent() </span> API를 사용할 수 있습니다. 콜백 핸들러는 인수를 사용하지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> Adobe Analytics과 같은 이벤트 추적 시스템에서 처리할 수 있는 뷰어 내에서 이벤트가 발생할 때마다 트리거됩니다. 콜백 핸들러는 다음 인수를 허용합니다. </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String} </span> - 현재 사용되지 않습니다. </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String} </span> - 현재 사용되지 않습니다. </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String} </span> - 이벤트를 트리거한 Viewer SDK 구성 요소의 인스턴스 이름입니다. </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> 타임스탬프 {Number} </span> - 이벤트 타임스탬프. </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String} </span> - 이벤트 페이로드. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate </span> </p> </td> 
   <td colname="col2"> <p> 사용자가 연결된 빠른 보기 데이터가 있는 핫스팟을 활성화하면 트리거됩니다. 콜백 핸들러는 다음 인수를 사용합니다. </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> 데이터 {Object} </span> - 핫스팟 정의의 데이터가 포함된 JSON 개체입니다. 필드 <span class="codeph"> sku </span>은(는) 필수이지만 다른 필드는 선택 사항이며 원본 핫스팟 정의에 따라 다릅니다. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

[CarouselViewer**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-carouselviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) 및 [setHandlers**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)도 참조하세요.
