---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,스핀 세트
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소재설정  </span> </p> </td> 
   <td colname="col2"> <p> 스핀 작업에 대한 두 번 클릭/탭 매핑을 구성합니다. <span class="codeph"> none </span> 으로 설정하면 두 번 클릭/탭 스핀을 사용할 수 없습니다. <span class="codeph"> 확대/축소 </span> 로 설정하면 이미지를 클릭하는 작업이 한 스핀 단계에서 회전됩니다. Ctrl 키를 누른 채로 클릭하면 한 스핀 단계가 회전됩니다. <span class="codeph"> 재설정 </span>으로 설정하면 이미지를 한 번 클릭하여 스핀을 초기 스핀 수준으로 재설정합니다. <span class="codeph"> zoomReset </span>의 경우, 현재 스핀 팩터가 지정된 제한을 초과하는 경우 재설정이 적용되며, 그렇지 않은 경우에는 스핀(spin)이 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-924163cb2f6542499f49894becef7fb5}

선택 사항입니다.

## 기본값 {#section-7a2128fd488941948aff18421f533ccf}

`reset` 데스크톱 컴퓨터에서  `zoomReset` 터치 장치

## 예 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
