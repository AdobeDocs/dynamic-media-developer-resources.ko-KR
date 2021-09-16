---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 숫자|점선</span> </p> </td> 
   <td colname="col2"> <p> 집합 표시기의 렌더링 스타일을 구성합니다. </p> <p><span class="codeph"> 점선 </span>으로 설정하면 구성 요소는 모든 페이지에 대해 동일한 표시기를 렌더링합니다. </p> <p><span class="codeph"> numeric</span>로 설정하면 각 표시기 요소 내에 1개 기반 페이지 번호가 배치됩니다. </p> <p><span class="codeph"> 숫자</span> 작업 모드는 터치 입력이 있는 장치에서 지원되지 않습니다. 대신 구성 요소는 이러한 장치에서 <span class="codeph"> 점선</span>을 사용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
