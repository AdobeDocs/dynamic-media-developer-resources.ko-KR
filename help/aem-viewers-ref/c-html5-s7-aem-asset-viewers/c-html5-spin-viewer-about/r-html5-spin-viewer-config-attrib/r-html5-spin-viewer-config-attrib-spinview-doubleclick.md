---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소 재설정 </span> </p> </td> 
   <td colname="col2"> <p> 회전 작업을 두 번 클릭/탭하여 매핑하도록 구성합니다. <span class="codeph"> 없음 </span>(으)로 설정하면 두 번 클릭/탭 회전이 비활성화됩니다. <span class="codeph"> 확대/축소 </span>(으)로 설정된 경우 이미지를 클릭하면 1회전 단계로 회전하고, Ctrl 키를 누른 상태에서 클릭하면 1회전 단계로 회전합니다. <span class="codeph"> 재설정 </span>(으)로 설정하면 이미지를 한 번 클릭할 때 스핀이 초기 회전 수준으로 재설정됩니다. <span class="codeph"> zoomReset </span>의 경우 현재 회전 비율이 지정된 제한에 도달하거나 초과할 경우 재설정이 적용되며 그렇지 않은 경우에는 회전이 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-924163cb2f6542499f49894becef7fb5}

선택적.

## 기본값 {#section-7a2128fd488941948aff18421f533ccf}

데스크톱 컴퓨터에서는 `reset`이고, 터치 장치에서는 `zoomReset`입니다.

## 예 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
