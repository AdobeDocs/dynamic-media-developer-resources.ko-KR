---
title: VideoViewer
description: 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 4ba152e6-b5a9-4e81-b9f8-aa987a1c31f9
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 3%

---

# VideoViewer{#videoviewer}

비디오 뷰어에 대한 JavaScript API 참조.

`VideoViewer([config])`

생성자, 새 비디오 뷰어 인스턴스를 만듭니다.

## 매개 변수 {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> 선택적 JSON 구성 개체를 사용하면 모든 뷰어 설정을 생성자에 전달하고 개별 setter 메서드를 호출하지 않을 수 있습니다. 다음 속성을 포함합니다. </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> DOM 컨테이너 ID(일반적으로 <span class="codeph"> DIV </span>)에 뷰어를 삽입합니다. 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요는 없습니다. 단, 컨테이너는 다음과 같은 경우에 존재해야 합니다. <span class="codeph"> init() </span> 가 실행되었습니다. 필수. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> 매개 변수 </span> - <span class="codeph"> {Object} </span> 속성 이름이 뷰어별 구성 옵션 또는 SDK 수정자이고 해당 속성 값이 해당 설정 값인 뷰어 구성 매개 변수가 있는 JSON 개체입니다. 필수. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> 핸들러 </span> - <span class="codeph"> {Object} </span> 속성 이름이 지원되는 뷰어 이벤트 이름이고 속성 값이 적절한 콜백에 대한 JavaScript 함수 참조인 뷰어 이벤트 콜백이 있는 JSON 개체입니다. 선택적. <p>다음을 참조하십시오 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-event-callbacks.md#concept-ebe5a4c1853d4912a919d86df35c1f6d" format="dita" scope="local"> 이벤트 콜백 </a> 뷰어 이벤트에 대한 자세한 정보. </p> </li> 
      <li id="li_D344288C9B584E569F7BF92D960F9DF8"> <p> <span class="codeph"> 지역화된 텍스트 </span> - { <span class="codeph"> 오브젝트 </span>현지화 데이터가 있는 } JSON 개체. 선택적. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-namespace.md#concept-679bfabb3e3e4c12a285c4e9c4144153" format="dita" scope="local"> Viewer SDK 네임스페이스 </a> 추가 정보. </p> <p>다음을 참조하십시오. <i>Viewer SDK 사용 안내서</i> 객체의 컨텐트에 대한 자세한 내용은 예제를 참조하십시오. 선택적. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
