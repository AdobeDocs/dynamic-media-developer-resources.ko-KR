---
title: Adobe Analytics 추적 지원
description: 기본 확대/축소 뷰어는 즉시 Adobe Analytics 추적을 지원합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 5b9d871d-9f37-4908-900e-3f0ecc98bc0c
TQID: 'https://experienceleague.adobe.com/SQ8j7yfYkRJ-thPAqD-vr8-JxzBQs1h2ZkME-4dJPtA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 0%

---

# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

기본 확대/축소 뷰어는 즉시 Adobe Analytics 추적을 지원합니다.

## 기본 제공 추적 {#section-ba994f079d0343c8ae48adffaa3195a3}

기본 확대/축소 뷰어는 [!DNL Adobe Analytics] 기본 추적을 지원합니다. 추적을 사용하려면 올바른 회사 사전 설정 이름을 `config2` 매개 변수로 전달하십시오.

뷰어는 또한 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버에 단일 추적 HTTP 요청을 보냅니다.

## 사용자 지정 추적 {#section-cda48fc9730142d0bb3326bac7df3271}

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백을 수신하고 필요에 따라 콜백 함수의 `eventInfo` 인수를 처리해야 합니다. 다음 코드는 이러한 처리기 함수의 예입니다.

```javascript {.line-numbers}
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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
 </tbody> 
</table>
