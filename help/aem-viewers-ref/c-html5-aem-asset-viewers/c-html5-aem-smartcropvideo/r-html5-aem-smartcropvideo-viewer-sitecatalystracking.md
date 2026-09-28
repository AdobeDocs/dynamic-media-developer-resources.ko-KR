---
title: Adobe Analytics 추적 지원
description: 스마트 자르기 비디오 뷰어는 즉시 사용할 수 있는 Adobe Analytics 추적을 지원합니다.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0d91ca94-79fc-40de-8095-0252688ebe76
TQID: 'https://experienceleague.adobe.com/qxJCNOQ6B6iYDi7JRepZfc9gMaF4Wn50DoPYWnTsq5Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%
---
# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

스마트 자르기 비디오 뷰어는 즉시 사용할 수 있는 Adobe Analytics 추적을 지원합니다.

## 기본 제공 추적 {#section-3b101fe30be943c1b679fd5c273569ca}

스마트 자르기 비디오 뷰어는 즉시 사용할 수 있는 Adobe Analytics 추적을 지원합니다.

추적을 사용하려면 올바른 회사 사전 설정 이름을 `config2` 매개 변수로 전달하십시오.

뷰어는 또한 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버에 단일 추적 HTTP 요청을 보냅니다.

## 사용자 지정 추적 {#section-ab10bd7caf184721a366cf3953071934}

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백을 수신하고 필요에 따라 콜백 함수의 `eventInfo` 인수를 처리해야 합니다. 다음 코드는 이러한 처리기 함수의 예입니다.

```javascript {.line-numbers}
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
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
   <td colname="col1"> <p> <span class="codeph"> 재생 </span> </p> </td> 
   <td colname="col2"> <p>재생이 시작되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 일시 중지 </span> </p> </td> 
   <td colname="col2"> <p>재생이 일시 중지되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> 중지 </p> </td> 
   <td colname="col2"> <p>재생이 중지됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 마일스톤 </span> </p> </td> 
   <td colname="col2"> <p>재생은 0%, 25%, 50%, 75% 및 100% 맷돌 중 하나에 도달합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
