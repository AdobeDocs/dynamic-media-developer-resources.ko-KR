---
description: 비디오 뷰어는 Adobe Analytics 즉시 사용 가능한 추적을 지원합니다.
seo-description: 비디오 뷰어는 Adobe Analytics 즉시 사용 가능한 추적을 지원합니다.
seo-title: Adobe Analytics 추적 지원
solution: Experience Manager
title: Adobe Analytics 추적 지원
uuid: c53b3d3b-42e5-4c87-8a1e-87c73eb32341
feature: Dynamic Media Classic,뷰어,SDK/API,비디오
role: 개발자,비즈니스 전문가,데이터 엔지니어,데이터 아키텍트
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 3%

---


# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

비디오 뷰어는 Adobe Analytics 즉시 사용 가능한 추적을 지원합니다.

## 즉시 사용 가능한 추적 {#section-3b101fe30be943c1b679fd5c273569ca}

비디오 뷰어는 Adobe Analytics 즉시 사용 가능한 추적을 지원합니다.

추적을 활성화하려면 적절한 회사 사전 설정 이름을 `config2` 매개 변수로 전달합니다.

뷰어는 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버에 단일 추적 HTTP 요청을 보냅니다.

## 사용자 지정 추적 {#section-ab10bd7caf184721a366cf3953071934}

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백을 수신하고 필요한 경우 콜백 함수의 `eventInfo` 인수를 처리해야 합니다. 다음 코드는 이러한 핸들러 함수의 예입니다.

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
   <td colname="col2"> <p>뷰어를 먼저 로드합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>뷰어에서 <span class="codeph"> setAsset() </span> API를 사용하여 에셋이 교체되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PLAY </span> </p> </td> 
   <td colname="col2"> <p>재생이 시작되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSE </span> </p> </td> 
   <td colname="col2"> <p>재생이 일시 중지됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOP </span> </p> </td> 
   <td colname="col2"> <p>재생이 중지됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>재생이 다음 항목 중 하나에 도달합니다.0%, 25%, 50%, 75%, 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

