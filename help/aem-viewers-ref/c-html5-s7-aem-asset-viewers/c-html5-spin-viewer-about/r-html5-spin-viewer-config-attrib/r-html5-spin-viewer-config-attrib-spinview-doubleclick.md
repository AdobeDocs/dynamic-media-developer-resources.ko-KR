---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소 재설정  </span> </p> </td> 
   <td colname="col2"> <p> 회전 동작에 대한 두 번 클릭/탭 매핑을 구성합니다. <span class="codeph"> none </span>으로 설정하면 두 번 클릭/탭 회전을 사용할 수 없습니다. <span class="codeph"> zoom </span>으로 설정된 경우 이미지를 클릭하는 것은 한 회전 단계에서 회전합니다.Ctrl+Click은 한 회전 단계를 축소합니다. <span class="codeph"> 재설정 </span>으로 설정하면 이미지를 한 번 클릭하면 회전이 초기 회전 수준으로 재설정됩니다. <span class="codeph"> zoomReset </span>의 경우 현재 스핀 인수가 지정된 한도 이상이면 재설정이 적용되며, 그렇지 않은 경우 회전이 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-924163cb2f6542499f49894becef7fb5}

선택 사항입니다.

## 기본값 {#section-7a2128fd488941948aff18421f533ccf}

`reset` 데스크톱 컴퓨터에; `zoomReset` 터치 디바이스에서 사용

## 예 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
