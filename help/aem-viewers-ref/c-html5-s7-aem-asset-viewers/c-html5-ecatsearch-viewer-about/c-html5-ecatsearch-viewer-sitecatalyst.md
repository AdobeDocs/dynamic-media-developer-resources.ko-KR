---
description: eCatalog 검색 뷰어는 즉시 Adobe Analytics 추적을 지원합니다.
solution: Experience Manager
title: Adobe Analytics 추적 지원
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User,Data Engineer,Data Architect
exl-id: b35e52f5-fa08-4945-aa52-9fdf41a6081a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 4%

---

# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

eCatalog 검색 뷰어는 즉시 Adobe Analytics 추적을 지원합니다.

## 기본 제공 추적 {#section-ba994f079d0343c8ae48adffaa3195a3}

eCatalog 검색 뷰어는 [!DNL Adobe Analytics] 즉시 추적. 추적을 활성화하려면 적절한 회사 사전 설정 이름을 (으)로 전달합니다. `config2` 매개 변수.

뷰어는 또한 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버에 단일 추적 HTTP 요청을 보냅니다.

## 사용자 지정 추적 {#section-cda48fc9730142d0bb3326bac7df3271}

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백 및 프로세스 `eventInfo` 필요에 따라 콜백 함수의 인수입니다. 다음 코드는 이러한 처리기 함수의 예입니다.

```javascript {.line-numbers}
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
   <td colname="col2"> <p>에셋은 뷰어에서 를 사용하여 교체됩니다. <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 확대/축소 </span> </p> </td> 
   <td colname="col2"> <p> 이미지가 확대/축소됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패닝 </span> </p> </td> 
   <td colname="col2"> <p>이미지가 패닝되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 견본 </span> </p> </td> 
   <td colname="col2"> <p> 견본을 클릭하거나 탭하여 이미지가 변경됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAGE </span> </p> </td> 
   <td colname="col2"> <p> 현재 프레임은 기본 보기에서 변경됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 항목 </span> </p> </td> 
   <td colname="col2"> <p>정보 패널 팝업이 활성화됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>사용자가 이미지 맵을 클릭하기 때문에 다른 페이지로 이동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
