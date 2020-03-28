---
description: 널
seo-description: 널
seo-title: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic media
uuid: 7af5e3d3-40c2-4f02-94e2-0314b698905d
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>정보 서버 URL 템플릿은 정보 패널 콘텐트 템플릿에서 변수 대체에 대한 키/값 쌍을 가져오는 데 사용됩니다.지정된 템플릿에는 일반적으로 요청이 서버로 전송되기 전에 실제 데이터로 대체되는 매크로 자리 표시자가 포함됩니다. </p> <p><span class="codeph"> $1$</span> 는 InfoPanelPopup 활성화를 트리거한 롤오버 값으로 <span class="codeph"> 대체됩니다</span> . </p> <p><span class="codeph"> $2$</span> 가 이미지 세트에 있는 현재 프레임의 시퀀스 번호로 바뀝니다. </p> <p><span class="codeph"> $3$</span> 는 현재 항목의 상위 세트 이름에 지정된 첫 번째 경로 요소로 대체됩니다. 일반적으로 카탈로그 ID에 해당합니다. </p> <p><span class="codeph"> $4$</span> 는 경로에서 다음 요소로 대체되며 자산 ID에 해당합니다. 실제 정보 서버 요청 구문은 정보 서버에 따라 다르며 서버마다 다릅니다. 예를 들어 다음은 일반적인 Scene7 정보 서버 요청 템플릿입니다. </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>정보 패널 팝업을 구성할 때 정보 패널에 전달된 HTML 코드 및 JavaScript 코드가 클라이언트의 컴퓨터에서 실행된다는 점에 유의하십시오. 따라서 이러한 HTML 코드와 JavaScript 코드가 안전한지 확인하십시오.

## 속성 {#section-71356e3c13244e62b0582980d9d05328}

선택 사항입니다.

## 기본값 {#section-22e9af803f724434807d34e200eb7518}

없음.

## 예 {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
