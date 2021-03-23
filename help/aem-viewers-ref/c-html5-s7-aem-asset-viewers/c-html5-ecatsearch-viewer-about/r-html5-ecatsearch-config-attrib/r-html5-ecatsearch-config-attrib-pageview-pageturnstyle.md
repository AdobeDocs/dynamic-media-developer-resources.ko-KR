---
description: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
uuid: 748adb73-bfb6-4fce-aa6a-4216184edabb
feature: Dynamic Media Classic,뷰어,SDK/API,eCatalog 검색
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

[!DNL `[PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWidthdividerColordividerOpacityborderOnOffborderColorfillColor`*`]

데스크톱 시스템에서 [!DNL `PageView.frametransition`]이(가) [!DNL `turn`] 또는 [!DNL `auto`]로 설정된 경우 구성 요소 모양을 제어합니다.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> 스프레드에서 왼쪽 및 오른쪽 페이지를 구분하는 페이지 분할자 그림자의 폭(픽셀)입니다. 또한 선반가공 페이지 옆에 표시된 실행 중인 그림자의 너비를 제어합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> RGGBB 형식의 그림자 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 0</span> 범위의 그림자 불투명도를 <span class="codeph"> 1</span>으로 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> 선반가공 페이지 주위의 테두리를 켜거나 끄는 플래그(<span class="codeph"> 0</span> 또는 <span class="codeph"> 1</span>)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB 형식의 테두리 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> 페이지 전환 애니메이션 시 사용되는 구성 요소 영역의 단색 채우기(RRGGBB 형식)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-54c634116cfe4f17813318e07539264c}

선택 사항입니다.

## 기본값 {#section-43fd13f639c2480c82658fafeeaf0846}

[!DNL `40,909090,1,1,909090,FFFFFF`]

## 예제 {#section-bb97b2aac37a43eba11d263ce7049363}

[!DNL `pageturnstyle=20,FF0000,1,1,00FF00,0000FF`]
