---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
TQID: 'https://experienceleague.adobe.com/en4zktUgJGVG-e0fahRGTxasP3CVxhgfie6d0e3q6r4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>정보 서버 URL 템플릿은 정보 패널 컨텐츠 템플릿에서 변수 대체를 위한 키/값 쌍을 가져오는 데 사용됩니다. 지정된 템플릿에는 일반적으로 요청을 서버로 보내기 전에 실제 데이터로 대체되는 매크로 자리 표시자가 포함됩니다. </p> <p><span class="codeph"> $1$</span>이(가) <span class="codeph"> InfoPanelPopup</span> 활성화를 트리거한 롤오버 값으로 대체되었습니다. </p> <p><span class="codeph"> $2$</span>이(가) 이미지 집합에서 현재 프레임의 시퀀스 번호로 대체되었습니다. </p> <p><span class="codeph"> $3$</span>이(가) 현재 항목의 부모 집합 이름에 지정된 첫 번째 경로 요소로 대체되었습니다. 일반적으로 카탈로그 ID에 해당합니다. </p> <p><span class="codeph"> $4$</span>이(가) 경로의 다음 요소로 대체되었으며 자산 id에 해당합니다. 실제 정보 서버 요청 구문은 정보 서버에 따라 다르며 서버마다 다릅니다. 예를 들어 다음은 일반적인 Dynamic Media 정보 서버 요청 템플릿입니다. </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>정보 패널 팝업을 구성할 때 정보 패널에 전달된 HTML 코드와 JavaScript 코드가 클라이언트의 컴퓨터에서 실행됩니다. 따라서 이러한 HTML 코드 및 JavaScript 코드가 안전한지 확인하십시오.

## 속성 {#section-71356e3c13244e62b0582980d9d05328}

선택적.

## 기본값 {#section-22e9af803f724434807d34e200eb7518}

없음.

## 예 {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
