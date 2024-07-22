---
title: Adobe Analytics 추적 지원
description: 스핀 뷰어는 즉시 사용 가능한 Adobe Analytics 추적을 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User,Data Engineer,Data Architect
exl-id: 30762700-6d69-4299-9492-57893232abe1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

스핀 뷰어는 즉시 사용 가능한 Adobe Analytics 추적을 지원합니다.

## 기본 제공 추적 {#section-d06145cfa2b9491bb485b599368d466e}

회전 뷰어는 즉시 사용할 수 있는 Adobe Analytics 추적을 지원합니다.

추적을 사용하려면 올바른 회사 사전 설정 이름을 `config2` 매개 변수로 전달하십시오.

뷰어는 또한 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버에 단일 추적 HTTP 요청을 보냅니다.

## 사용자 지정 추적 {#section-47512156a1d64b338b50cfa39c84f4aa}

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백을 수신하고 필요에 따라 콜백 함수의 `eventInfo` 인수를 처리해야 합니다. 다음 코드는 이러한 처리기 함수의 예입니다.

```javascript {.line-numbers}
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
   <th colname="col2" class="entry"> <p>전송 시점... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> 로드 </p> </td> 
   <td colname="col2"> <p>뷰어가 먼저 로드됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 교체 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> setAsset() </span> API를 사용하여 뷰어에서 자산을 바꿨습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 확대/축소 </span> </p> </td> 
   <td colname="col2"> <p> 이미지가 확대/축소됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 팬 </span> </p> </td> 
   <td colname="col2"> <p>이미지가 패닝되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 회전 </span> </p> </td> 
   <td colname="col2"> <p> 스핀이 수행됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
