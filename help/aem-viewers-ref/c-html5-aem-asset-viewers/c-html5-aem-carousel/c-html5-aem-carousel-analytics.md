---
description: Adobe Analytics 추적 지원
solution: Experience Manager
title: Adobe Analytics 추적 지원
feature: Dynamic Media Classic,뷰어,SDK/API,회전판 배너
role: 개발자,비즈니스 전문가,데이터 엔지니어,데이터 아키텍트
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---


# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

## 사용자 지정 추적 {#section-cda48fc9730142d0bb3326bac7df3271}

기본적으로 뷰어는 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버에 단일 추적 HTTP 요청을 보냅니다.

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백을 수신하고 필요한 경우 콜백 함수의 `eventInfo` 인수를 처리해야 합니다. 다음 코드는 이러한 핸들러 함수의 예입니다.

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
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
   <th colname="col2" class="entry"> <p>전송 시기... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>뷰어가 먼저 로드됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배너  </span> </p> </td> 
   <td colname="col2"> <p>회전판 배너 이미지가 변경되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>사용자가 핫스팟을 활성화합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

