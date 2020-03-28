---
description: eCatalog 검색 뷰어는 즉시 사용 가능한 Adobe Analytics 추적을 지원합니다.
seo-description: eCatalog 검색 뷰어는 즉시 사용 가능한 Adobe Analytics 추적을 지원합니다.
seo-title: Adobe Analytics 추적 지원
solution: Experience Manager
title: Adobe Analytics 추적 지원
topic: Dynamic media
uuid: 2e1e2bc6-5372-4ba2-b6d7-8b760b1b0a8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Adobe Analytics 추적 지원{#support-for-adobe-analytics-tracking}

eCatalog 검색 뷰어는 즉시 사용 가능한 Adobe Analytics 추적을 지원합니다.

## 즉시 사용 가능한 추적 {#section-ba994f079d0343c8ae48adffaa3195a3}

eCatalog 검색 뷰어는 즉시 사용 가능한 [!DNL Adobe Analytics] 추적을 지원합니다. 추적을 활성화하려면 적절한 회사 사전 설정 이름을 `config2` 매개 변수로 전달합니다.

또한 뷰어는 뷰어 유형 및 버전 정보와 함께 구성된 이미지 서버에 단일 추적 HTTP 요청을 보냅니다.

## 사용자 지정 추적 {#section-cda48fc9730142d0bb3326bac7df3271}

타사 분석 시스템과 통합하려면 `trackEvent` 뷰어 콜백을 수신하고 필요한 경우 콜백 함수의 `eventInfo` 인수를 처리해야 합니다. 다음 코드는 이러한 처리기 함수의 예입니다.

```
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
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
   <td colname="col2"> <p>뷰어가 먼저 로드됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>setAsset() API를 사용하여 뷰어에서 자산이 <span class="codeph"> 교체됩니다 </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 확대/축소 </span> </p> </td> 
   <td colname="col2"> <p> 이미지가 확대됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패닝 </span> </p> </td> 
   <td colname="col2"> <p>이미지가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 견본 </span> </p> </td> 
   <td colname="col2"> <p> 견본을 클릭하거나 탭하여 이미지가 변경됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAGE </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기에서 현재 프레임이 변경됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 항목 </span> </p> </td> 
   <td colname="col2"> <p>정보 패널 팝업이 활성화됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>사용자가 이미지 맵을 클릭하여 다른 페이지로 이동합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

