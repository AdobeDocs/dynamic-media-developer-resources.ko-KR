---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
TQID: 'https://experienceleague.adobe.com/lss5EqVS8ggpyoDlnGlcagfln977-Hw4fcchN5LMGt4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 4%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 숫자|dotted</span> </p> </td> 
   <td colname="col2"> <p> 설정된 표시기의 렌더링 스타일을 구성합니다. </p> <p><span class="codeph"> 점선 </span>(으)로 설정하면 구성 요소가 모든 페이지에 대해 동일한 지표를 렌더링합니다. </p> <p><span class="codeph"> numeric</span>(으)로 설정된 경우 각 표시기 요소 안에 1부터 시작하는 페이지 번호를 설정합니다. </p> <p>터치 입력이 있는 장치에서는 <span class="codeph"> numeric</span> 작업 모드가 지원되지 않습니다. 대신 구성 요소는 이러한 장치에서 <span class="codeph"> dotted</span>을(를) 사용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
