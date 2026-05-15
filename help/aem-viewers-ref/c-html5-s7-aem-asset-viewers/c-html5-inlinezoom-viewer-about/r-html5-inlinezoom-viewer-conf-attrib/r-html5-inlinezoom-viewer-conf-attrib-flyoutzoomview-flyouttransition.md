---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 3199d4a3-4799-40a2-b0a5-0e1ee4744fbe
TQID: 'https://experienceleague.adobe.com/FOK4Eoi3n-7LWZeJwciRFfkPTTnsrF-v-XI7APHiQIs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 2%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`showtime`*[, *`showdelay`*[, *`hidetime`*[, *`hidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 없음|슬라이드|페이드 </span> </span> </p> </td> 
   <td colname="col2"> <p> 플라이아웃 보기가 표시되거나 숨겨지면 적용되는 효과의 유형을 지정합니다. <span class="codeph"> 없음 </span>에서 플라이아웃 이미지는 활성화 및 준비 시 즉시 나타납니다. <span class="codeph"> 슬라이드 </span>에서는 슬라이드 애니메이션이 왼쪽에서 오른쪽 방향으로 재생됩니다. <span class="codeph"> 페이드 </span>에서는 플라이아웃 이미지에 알파 전환을 적용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 표시가 완료되는 데 소요되는 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 표시를 시작하는 사용자 동작과 애니메이션 표시 자체의 시작 간 지연 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 숨김 시간 </span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 숨기기가 완료되는 데 소요되는 시간(초)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지연 숨기기 </span> </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 숨기기를 시작하는 사용자 동작과 애니메이션 숨기기 자체의 시작 간 지연 시간(초)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택적.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
