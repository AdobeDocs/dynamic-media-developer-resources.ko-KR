---
title: CarouselView.enableHD
description: CarouselView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
TQID: 'https://experienceleague.adobe.com/oMOwi3bg8BRBlxWBtUIg5mCD3Q45Vo-cCISF87XB8m0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 3%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`숫자`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 항상|제한 안 함|제한</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> devicePixelRatio</span>이 <span class="codeph"> 1</span>보다 큰 장치, 즉, iPhone4 및 이와 유사한 장치와 같이 고밀도 디스플레이를 사용하는 장치의 최적화를 활성화, 제한 또는 비활성화합니다. </p> <p>활성화하면 구성 요소가 장치의 픽셀 비율이 <span class="codeph"> 1</span>인 것처럼 IS 이미지 요청의 크기를 제한하여 대역폭을 줄입니다. </p> <p>아래 예를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 숫자</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 제한</span> 설정을 사용하는 경우 구성 요소는 높은 픽셀 밀도를 지정된 제한까지만 활성화합니다. </p> <p>아래 예를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
