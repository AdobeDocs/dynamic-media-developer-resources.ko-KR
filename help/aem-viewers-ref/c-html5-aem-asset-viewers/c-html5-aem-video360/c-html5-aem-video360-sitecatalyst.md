---
title: Adobe Analytics 추적 지원
description: Adobe Analytics 추적 지원
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
TQID: 'https://experienceleague.adobe.com/dpuF-Ph89--e--bNIEx4RnAjmCdPLfw1i4YDdi-YHZc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 0%

---

# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

기본적으로 뷰어는 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버에 단일 추적 HTTP 요청을 보냅니다.

## 사용자 지정 추적 {#section-cda48fc9730142d0bb3326bac7df3271}

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백을 수신하고 필요에 따라 콜백 함수의 `eventInfo` 인수를 처리해야 합니다. 다음 코드는 이러한 처리기 함수의 예입니다.

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
   <th colname="col2" class="entry"> <p>보냄... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> 로드 </p> </td> 
   <td colname="col2"> <p>뷰어가 먼저 로드되는 경우입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 교체 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> setAsset() </span> API를 사용하여 뷰어에서 자산을 스왑하는 경우. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 재생 </span> </p> </td> 
   <td colname="col2"> <p>재생이 시작되는 시기 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 일시 중지 </span> </p> </td> 
   <td colname="col2"> <p>재생이 일시 중지된 경우. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> 중지 </p> </td> 
   <td colname="col2"> <p>재생이 중지되는 경우입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 마일스톤 </span> </p> </td> 
   <td colname="col2"> <p>재생이 0%, 25%, 50%, 75% 또는 100% 이정표 중 하나에 도달하는 경우. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 대화형 견본 </span> </p> </td> 
   <td colname="col2"> <p>사용자가 대화형 견본을 클릭할 때마다 </p> </td> 
  </tr> 
 </tbody> 
</table>
