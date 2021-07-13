---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,User
exl-id: c2aeb45f-879b-4a53-b571-744fc73d04fd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 2D 스핀 세트의 경우 스핀 방향을 변경할지 여부를 지정합니다. </p> <p><span class="codeph"> 1 </span>로 설정하면 구성 요소는 제스처의 시작 시 기본 드래그 또는 밀기 방향(가로 및 세로)을 식별합니다. 이후 제스처가 종료될 때까지 해당 방향을 유지합니다. 예를 들어 사용자가 수평 스핀을 시작한 다음 수직 방향으로 드래그 제스처를 계속하기로 결정하는 경우, 구성 요소는 수직 스핀을 수행하지 않습니다. 대신 마우스나 스와이프의 수평 이동만 고려합니다. </p> <p><span class="codeph"> 0 </span> 값을 사용하면 제스처 진행 중에 언제든지 스핀 방향을 변경할 수 있습니다. 스핀 세트가 1D인 경우에는 설정이 영향을 주지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
