---
description: HTML5 Video360 뷰어는 Adobe Analytics 즉시 사용 가능한 추적을 지원합니다.
solution: Experience Manager
title: Adobe Analytics 추적 지원
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner,Data Engineer,Data Architect
exl-id: 74a69d01-fa58-4d36-8598-992baf6ae11d
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 3%

---

# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

HTML5 Video360 뷰어는 Adobe Analytics 즉시 사용 가능한 추적을 지원합니다.

추적을 활성화하려면 적절한 회사 사전 설정 이름을 `config2` 매개 변수로 전달합니다.

기본적으로 뷰어는 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버로 단일 추적 HTTP 요청을 전송합니다.

## 사용자 지정 추적 {#section-cda48fc9730142d0bb3326bac7df3271}

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백을 수신하고 필요한 경우 콜백 함수의 `eventInfo` 인수를 처리해야 합니다. 다음 코드는 이러한 핸들러 함수의 예입니다.

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
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
 </tbody> 
</table>
