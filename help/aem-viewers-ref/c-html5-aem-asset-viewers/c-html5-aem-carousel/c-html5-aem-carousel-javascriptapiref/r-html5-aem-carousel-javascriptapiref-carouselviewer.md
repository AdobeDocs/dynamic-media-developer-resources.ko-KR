---
description: 회전판 뷰어에 대한 JavaScript API 참조입니다.
seo-description: 회전판 뷰어에 대한 JavaScript API 참조입니다.
seo-title: CarouselViewer
solution: Experience Manager
title: CarouselViewer
topic: Dynamic media
uuid: 443a5b54-b5f6-4594-810b-ce9b2ba40611
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 3%

---


# CarouselViewer{#carouselviewer}

회전판 뷰어에 대한 JavaScript API 참조입니다.

`CarouselViewer([config])`

생성자가 새 HTML 5 회전판 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object}  </span> 선택 사항인 JSON 구성 객체를 사용하면 모든 뷰어 설정이 생성자에게 전달되어 개별 setter 메서드를 호출하지 않도록 할 수 있습니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> 뷰어가 삽입된 DOM 컨테이너(일반적으로  <span class="codeph"> DIV </span>)의 ID 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요가 없습니다. 그러나 <span class="codeph"> init() </span>가 실행될 때는 컨테이너가 존재해야 합니다. </p> <p>필수. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}  </span> JSON 개체에는 뷰어 구성 매개 변수가 있습니다. 여기서 속성 이름은 뷰어 특정 구성 옵션 또는 SDK 수정자이고 해당 속성의 값은 해당 설정 값입니다. </p> <p>필수. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 핸들러  </span> -  <span class="codeph"> {Object}  </span> JSON 개체(뷰어 이벤트 콜백을 사용하는 경우). 여기서 속성 이름은 지원되는 뷰어 이벤트의 이름이고 속성 값은 해당 콜백에 대한 JavaScript 함수 참조입니다. </p> <p>선택 사항입니다. </p> <p>뷰어 이벤트에 대한 자세한 내용은 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 이벤트 콜백 </a>을 참조하십시오. </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedText  </span> -  <span class="codeph"> {Object}  </span> </p> <p> 로컬라이제이션 데이터가 있는 JSON 개체입니다. 개체 컨텐츠에 대한 자세한 내용은 사용자 인터페이스 요소의 현지화 및 예제를 참조하십시오. </p> <p>선택 사항입니다 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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

