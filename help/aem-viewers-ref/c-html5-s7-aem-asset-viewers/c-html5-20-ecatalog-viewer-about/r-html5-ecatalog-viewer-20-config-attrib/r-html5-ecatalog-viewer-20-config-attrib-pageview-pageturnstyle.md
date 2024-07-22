---
title: PageView.pageturnstyle
description: PageView.pageturnstyle
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 00706c64-c051-4b62-8194-61d0a1c565e9
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *`분할선 너비`*, *`분할선 색상`*, *`분할선 불투명도`*, *`borderOnOff`*, *`borderColor`*, *`채우기 색상`*`

데스크톱 시스템에서 `PageView.frametransition`이(가) `turn` 또는 `auto`(으)로 설정된 경우 구성 요소 모양을 제어합니다.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> 스프레드에 있는 왼쪽 페이지와 오른쪽 페이지를 구분하는 페이지 구분선 그림자의 픽셀 단위 폭입니다. 또한 선반가공 페이지 옆에 표시되는 실행 중인 그림자의 너비를 제어합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB 형식의 그림자 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 0</span> - <span class="codeph"> 1</span> 범위의 그림자 불투명도입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> 전환 페이지 주변의 테두리를 켜거나 끄는 플래그(<span class="codeph"> 0</span> 또는 <span class="codeph"> 1</span>)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB 형식의 테두리 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> RRGGBB 형식의 페이지 넘기기 애니메이션 동안 사용되는 구성 요소 영역의 단색 채우기 색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-54c634116cfe4f17813318e07539264c}

선택적.

## 기본값 {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## 예제 {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
