---
description: 비디오 이미지 뷰어용 JavaScript API 참조.
seo-description: 비디오 이미지 뷰어용 JavaScript API 참조.
seo-title: InteractiveImage
solution: Experience Manager
title: InteractiveImage
topic: Dynamic media
uuid: 19bd0603-3180-4913-b5a0-93699c5131bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# InteractiveImage{#interactiveimage}

비디오 이미지 뷰어용 JavaScript API 참조.

`InteractiveImage([config])`

생성자가 새 비디오 이미지 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 구성 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> 선택적 JSON 구성 개체를 사용하면 모든 뷰어 설정이 생성자에 전달되어 개별 setter 메서드를 호출하지 않도록 할 수 있습니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerID </span> - <span class="codeph"> {String} </span> 뷰어가 삽입된 DOM 컨테이너( <span class="codeph"> 일반적으로 DIV </span>)의 ID. 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요가 없습니다. 그러나 <span class="codeph"> init()를 </span> 실행할 때는 컨테이너가 존재해야 합니다. </p> <p>필수. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON 개체(속성 이름이 뷰어 특정 구성 옵션 또는 SDK 수정자 중 하나이며 해당 속성의 값은 해당 설정 값입니다. </p> <p>필수. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 핸들러 </span> - <span class="codeph"> {Object} </span> 뷰어 이벤트 콜백이 있는 JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트의 이름이고 속성 값은 해당 콜백에 대한 JavaScript 함수 참조입니다. </p> <p>선택 사항입니다. </p> <p>뷰어 이벤트에 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 대한 자세한 내용은 이벤트 콜백을 </a> 참조하십시오. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
} 
});
```

