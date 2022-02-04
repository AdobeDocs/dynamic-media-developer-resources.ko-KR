---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소재설정 </span> </p> </td> 
   <td colname="col2"> <p> 스핀 작업에 대한 두 번 클릭/탭 매핑을 구성합니다. 설정 대상 <span class="codeph"> 없음 </span> 두 번 클릭/탭 스핀을 사용하지 않도록 설정합니다. 로 설정된 경우 <span class="codeph"> 확대/축소 </span>를 클릭하여 이미지를 한 회전 단계로 전환합니다. Ctrl 키를 누른 채로 클릭하면 한 스핀 단계가 회전됩니다. 설정 대상 <span class="codeph"> 재설정 </span> 이미지를 한 번 클릭하면 스핀을 초기 스핀 수준으로 재설정합니다. 대상 <span class="codeph"> zoomReset </span>, 재설정은 현재 스핀 팩터가 지정된 제한을 초과하는 경우 적용되며, 그렇지 않으면 스핀 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 데스크탑 컴퓨터 `zoomReset` 터치 장치

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
