---
title: 대화형 비디오 뷰어
description: 대화형 비디오 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: efd0ffea-482c-4af4-ac77-ac1b7f326ce9
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 3%

---

# 대화형 비디오 뷰어{#interactivevideoviewer}

대화형 비디오 뷰어에 대한 JavaScript API 참조입니다.

`InteractiveVideoViewer([config])`

생성자, 대화형 비디오 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 구성 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> 선택적 JSON 구성 개체로, 개별 setter 메서드를 호출하지 않도록 모든 뷰어 설정을 생성자에게 전달할 수 있습니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> 뷰어가 삽입되는 DOM 컨테이너(일반적으로 <span class="codeph"> DIV </span>)의 <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID. 이 메서드가 호출될 때 컨테이너 요소를 만들 필요가 없습니다. 그러나 <span class="codeph"> init() </span>을(를) 실행할 때는 컨테이너가 있어야 합니다. </p> <p>필수. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> 매개 변수 </span> - <span class="codeph"> {Object} </span> JSON 개체와 뷰어 구성 매개 변수 포함. 여기서 속성 이름은 뷰어별 구성 옵션 또는 SDK 한정자이고 해당 속성 값은 해당 설정 값입니다. </p> <p>필수. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> 처리기 </span> - <span class="codeph"> {Object} </span> 뷰어 이벤트 콜백이 있는 JSON 개체. 여기서 속성 이름은 지원되는 뷰어 이벤트 이름이고 속성 값은 적절한 콜백에 대한 JavaScript 함수 참조입니다. </p> <p>선택적. </p> <p>뷰어 이벤트에 대한 자세한 내용은 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> 이벤트 콜백 </a>을(를) 참조하십시오. </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> 로컬라이제이션 데이터가 있는 <span class="codeph"> localizedText </span> - <span class="codeph"> {Object} </span> JSON 개체. 선택적. </p> <p>자세한 내용은 사용자 인터페이스 요소 </a>의 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> 지역화를 참조하십시오. </p> <p>개체 콘텐츠에 대한 자세한 내용은 <i>Viewer SDK 사용 안내서</i>와 예제를 참조하십시오. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
