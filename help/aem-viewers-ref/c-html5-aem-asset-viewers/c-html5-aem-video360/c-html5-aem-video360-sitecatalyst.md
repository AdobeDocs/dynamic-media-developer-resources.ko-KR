---
description: 널
seo-description: 널
seo-title: Adobe Analytics 추적 지원
solution: Experience Manager
title: Adobe Analytics 추적 지원
topic: Dynamic media
uuid: 0d4dee7b-3ffb-4bf5-93b1-67972bfc9b2a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 5%

---


# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

기본적으로 뷰어는 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버로 단일 추적 HTTP 요청을 전송합니다.

## 사용자 지정 추적 {#section-cda48fc9730142d0bb3326bac7df3271}

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백을 수신하고 필요한 경우 콜백 함수의 `eventInfo` 인수를 처리해야 합니다. 다음 코드는 이러한 핸들러 함수의 예입니다.

```
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
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   case "INTERACTIVE_SWATCH": 
    //custom event processing code which handles user clicks on interactive swatches 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

뷰어는 다음 SDK 사용자 이벤트를 추적합니다.

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK 사용자 이벤트 </p> </th> 
   <th colname="col2" class="entry"> <p>전송 중... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>뷰어를 처음 불러오는 경우. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>뷰어에서 <span class="codeph"> setAsset() </span> API를 사용하여 에셋을 교환하는 경우 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>재생을 시작할 때 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>재생이 일시 정지될 때. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>재생이 중지되면 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>재생이 다음 이정표 중 하나에 도달하는 경우:0%, 25%, 50%, 75% 또는 100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> INTERACTIVE_SWATCH  </span> </p> </td> 
   <td colname="col2"> <p>사용자가 인터랙티브한 견본을 클릭할 때마다 </p> </td> 
  </tr> 
 </tbody> 
</table>

