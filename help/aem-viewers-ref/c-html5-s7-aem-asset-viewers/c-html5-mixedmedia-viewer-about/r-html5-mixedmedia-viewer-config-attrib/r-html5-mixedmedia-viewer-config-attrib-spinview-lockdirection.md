---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c2aeb45f-879b-4a53-b571-744fc73d04fd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 2D 스핀 세트가 있는 경우 스핀 방향을 변경할지 여부를 지정합니다. </p> <p>로 설정된 경우 <span class="codeph"> 1 </span>로 지정하는 경우 구성 요소는 제스처 시작 시 기본 드래그 또는 밀기 방향(가로 및 세로)을 식별합니다. 이후 제스처가 종료될 때까지 해당 방향을 유지합니다. 예를 들어 사용자가 수평 스핀을 시작한 다음 수직 방향으로 드래그 제스처를 계속하기로 결정하는 경우 구성 요소는 수직 스핀을 수행하지 않습니다. 대신 마우스나 스와이프의 수평 이동만 고려합니다. </p> <p>값 <span class="codeph"> 0 </span> 사용자가 제스처 진행 중에 언제든지 스핀 방향을 변경할 수 있도록 해줍니다. 스핀 세트가 1D인 경우에는 설정이 적용되지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
