---
description: 회전 뷰어는 즉시 사용 가능한 Adobe Analytics 추적을 지원합니다.
seo-description: 회전 뷰어는 즉시 사용 가능한 Adobe Analytics 추적을 지원합니다.
seo-title: Adobe Analytics 추적 지원
solution: Experience Manager
title: Adobe Analytics 추적 지원
topic: Dynamic media
uuid: 337671f0-22e8-4e3e-a0a9-ce49d271ea56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---


# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

회전 뷰어는 즉시 사용 가능한 Adobe Analytics 추적을 지원합니다.

## 즉시 사용 가능한 추적 {#section-d06145cfa2b9491bb485b599368d466e}

스핀 뷰어는 Adobe Analytics 즉시 사용 가능한 추적을 지원합니다.

추적을 활성화하려면 적절한 회사 사전 설정 이름을 `config2` 매개 변수로 전달합니다.

뷰어는 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버에 단일 추적 HTTP 요청을 보냅니다.

## 사용자 지정 추적 {#section-47512156a1d64b338b50cfa39c84f4aa}

타사 분석 시스템과 통합하려면 필요에 따라 `trackEvent` 뷰어 콜백을 수신하고 콜백 함수의 `eventInfo` 인수를 처리해야 합니다. 다음 코드는 이러한 핸들러 함수의 예입니다.

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
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
   <td colname="col1"> <p> <span class="codeph"> 확대/축소 </span> </p> </td> 
   <td colname="col2"> <p> 이미지가 확대되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패닝 </span> </p> </td> 
   <td colname="col2"> <p>이미지가 팬됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 회전 </span> </p> </td> 
   <td colname="col2"> <p> 회전이 수행됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

