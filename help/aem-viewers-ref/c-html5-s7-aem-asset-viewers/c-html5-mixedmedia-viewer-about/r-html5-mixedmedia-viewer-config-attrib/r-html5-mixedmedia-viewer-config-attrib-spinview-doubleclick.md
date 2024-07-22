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
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소 재설정 </span> </p> </td> 
   <td colname="col2"> <p> 회전 작업을 두 번 클릭/탭하여 매핑하도록 구성합니다. <span class="codeph"> 없음 </span>(으)로 설정하면 두 번 클릭/탭 회전이 비활성화됩니다. <span class="codeph"> 확대/축소 </span>(으)로 설정된 경우 이미지를 클릭하면 1회전 단계로 회전하고, Ctrl 키를 누른 상태에서 클릭하면 1회전 단계로 회전합니다. <span class="codeph"> 재설정 </span>(으)로 설정하면 이미지를 한 번 클릭할 때 스핀이 초기 회전 수준으로 재설정됩니다. <span class="codeph"> zoomReset </span>의 경우 현재 회전 비율이 지정된 제한에 도달하거나 초과할 경우 재설정이 적용되며 그렇지 않은 경우에는 회전이 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

데스크톱 컴퓨터에서는 `reset`, 터치 장치에서는 `zoomReset`입니다.

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
