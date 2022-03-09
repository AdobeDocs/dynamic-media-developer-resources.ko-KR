---
title: 회전판 뷰어
description: 회전판 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 890d869d-dbf2-4c24-88d1-34c439ab1e3a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# 회전판 뷰어{#carouselviewer}

회전판 뷰어에 대한 JavaScript API 참조.

`CarouselViewer([config])`

생성자에서 HTML 5 회전 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> 선택 사항인 JSON 구성 개체를 사용하면 개별 setter 메서드를 호출하지 않도록 모든 뷰어 설정을 생성자에 전달할 수 있습니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> DOM 컨테이너의 ID(일반적으로 <span class="codeph"> DIV </span>) 뷰어가 삽입되는 위치에 포함될 수 있습니다. 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요가 없습니다. 그러나 이 컨테이너는 <span class="codeph"> init() </span> 가 실행됩니다. </p> <p>필수. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> 뷰어 구성 매개 변수가 있는 JSON 개체. 여기서 속성 이름은 뷰어별 구성 옵션 또는 SDK 수정자 이며 해당 속성의 값은 해당하는 설정 값입니다. </p> <p>필수. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 핸들러 </span> - <span class="codeph"> {Object} </span> 뷰어 이벤트 콜백이 있는 JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트의 이름이고 속성 값은 적절한 콜백에 대한 JavaScript 함수 참조입니다. </p> <p>선택 사항입니다. </p> <p>자세한 내용은 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 이벤트 콜백 </a> 뷰어 이벤트에 대한 자세한 정보. </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedText </span> - <span class="codeph"> {Object} </span> </p> <p> 로컬라이제이션 데이터가 있는 JSON 개체. 객체 컨텐츠에 대한 자세한 내용은 사용자 인터페이스 요소 현지화 및 예를 참조하십시오. </p> <p>선택 사항입니다 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left" 
}, 
"fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste" 
}, 
defaultLocale:"en" 
} 
});
```
