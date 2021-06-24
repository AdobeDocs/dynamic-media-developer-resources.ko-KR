---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,확대/축소
role: Developer,Business Practitioner
exl-id: 38c90d7f-ddbc-4123-b90d-02f9cabd785c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소재설정  </span> </p> </td> 
   <td colname="col2"> <p> 확대/축소 작업을 위한 두 번 클릭/탭 매핑을 구성합니다. <span class="codeph"> none </span> 으로 설정하면 확대/축소를 두 번 클릭/탭할 수 없습니다. <span class="codeph"> 확대/축소 </span> 로 설정하면 한 확대/축소 단계에서 이미지가 확대됩니다.Ctrl 키를 누른 상태에서 클릭하여 한 확대/축소 단계를 축소합니다. <span class="codeph"> 재설정 </span>으로 설정하면 이미지를 한 번 클릭하면 확대/축소가 초기 확대/축소 수준으로 재설정됩니다. <span class="codeph"> zoomReset </span>의 경우, 현재 확대/축소 비율이 지정된 제한을 초과하는 경우 재설정이 적용되며, 그렇지 않으면 확대/축소가 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-50bcd15223174bb79ce08b31ea03d682}

선택 사항입니다.

## 기본값 {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` 데스크톱 컴퓨터에서 `zoomReset` 터치 장치

## 예 {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
