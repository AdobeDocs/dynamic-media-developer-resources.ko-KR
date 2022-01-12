---
title: Adobe Analytics 추적 지원
description: 플라이아웃 뷰어는 Adobe Analytics 즉시 추적을 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User,Data Engineer,Data Architect
exl-id: 6b6216f4-34dc-496f-a0c3-e97d48da14c6
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 2%

---

# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

플라이아웃 뷰어는 Adobe Analytics 즉시 추적을 지원합니다.

## 기본 추적 {#section-ba994f079d0343c8ae48adffaa3195a3}

플라이아웃 뷰어가 지원합니다. [!DNL Adobe Analytics] 즉시 사용 가능한 추적. 추적을 활성화하려면 적절한 회사 사전 설정 이름을 `config2` 매개 변수.

또한 뷰어는 뷰어 유형 및 버전 정보로 구성된 이미지 서버에 단일 추적 HTTP 요청을 보냅니다.

## 사용자 지정 추적 {#section-cda48fc9730142d0bb3326bac7df3271}

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백 및 처리 `eventInfo` 필요한 경우 콜백 함수의 인수입니다. 다음 코드는 이러한 처리기 함수의 예입니다.

```
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
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
   <td colname="col1"> <p> <span class="codeph"> LOAD </span> </p> </td> 
   <td colname="col2"> <p>뷰어가 먼저 로드됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>뷰어에서 자산을 <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 확대/축소 </span> </p> </td> 
   <td colname="col2"> <p>플라이아웃이 활성화되거나 확대/축소 수준이 변경되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패닝 </span> </p> </td> 
   <td colname="col2"> <p> 이미지가 패닝됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 견본 </span> </p> </td> 
   <td colname="col2"> <p> 견본 을 클릭하거나 탭하여 이미지가 변경됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
