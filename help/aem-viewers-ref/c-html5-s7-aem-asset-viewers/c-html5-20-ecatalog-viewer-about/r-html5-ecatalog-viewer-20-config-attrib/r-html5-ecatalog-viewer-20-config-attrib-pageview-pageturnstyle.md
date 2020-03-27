---
description: 널
seo-description: 널
seo-title: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
topic: Dynamic media
uuid: 3192d810-fb30-44ae-9939-98e890c76e5c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWidthdividerColordividerOpacityborderOnOffborderColorfillColor`*`

데스크톱 시스템에서 구성 요소 모양을 `PageView.frametransition` 로 `turn` 또는 `auto` 로 설정할 때 구성 요소 모양을 제어합니다.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> 스프레드의 왼쪽 및 오른쪽 페이지를 구분하는 페이지 분할선 그림자의 너비(픽셀 단위)입니다. 또한 선반가공 페이지 옆에 표시되는 실행 그림자의 너비를 제어합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> RGGBB 형식의 그림자 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>그림자 불투명도( <span class="codeph"> 0</span> ~1 <span class="codeph"> )입니다</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> 선반가공 페이지 주위의 테두리를 켜거나 끄는 플래그( <span class="codeph"> 0</span> 또는 <span class="codeph"> 1</span>)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> RGGBB 형식의 테두리 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> 페이지 전환 시 사용되는 구성 요소 영역의 단색 채우기 색상은 RRGGBB 형식으로 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-54c634116cfe4f17813318e07539264c}

선택 사항입니다.

## 기본값 {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## 예제 {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
