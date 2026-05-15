---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 39cb629a-3940-4206-91cd-fe9a9f4d9f75
TQID: 'https://experienceleague.adobe.com/AX55D86n9ifbW-nRBlNZUW6WyTxVlGf5jlfTr6owRE4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 6%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`기간`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> 자산 변경 시 기본 보기에 적용되는 효과의 유형을 지정합니다. </p> <p><span class="codeph"> none</span>은(는) 전환이 없음을 나타내며 기본 보기 변경이 즉시 발생합니다. </p> <p><span class="codeph"> 페이드</span>는 이전 이미지가 페이드 아웃되고 새 이미지가 페이드 인되는 크로스페이드 전환을 활성화합니다 </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 기간</span></span> </p> </td> 
   <td colname="col2"> <p> 애니메이션이 완료되는 데 소요되는 시간(초)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택적.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

없음.

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`
