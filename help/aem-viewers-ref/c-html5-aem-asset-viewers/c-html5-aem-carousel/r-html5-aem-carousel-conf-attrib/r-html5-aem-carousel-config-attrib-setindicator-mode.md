---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
feature: Dynamic Media Classic,Viewers,SDK/API,회전 배너
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 숫자|점선</span> </p> </td> 
   <td colname="col2"> <p> 집합 표시기의 렌더링 스타일을 구성합니다. </p> <p><span class="codeph"> 점선</span>으로 설정하면 구성 요소는 모든 페이지에 대해 동일한 표시기를 렌더링합니다. </p> <p><span class="codeph"> numeric</span>로 설정하면 각 표시기 요소 내에 1개 기반 페이지 번호가 배치됩니다. </p> <p>터치 입력이 가능한 장치에서는 <span class="codeph"> 숫자</span> 작업 모드가 지원되지 않습니다. 대신 구성 요소는 이러한 장치에서 <span class="codeph"> 점선</span>을 사용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`dotted`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
