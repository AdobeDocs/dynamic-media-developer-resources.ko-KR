---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,Business Practitioner
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소재설정  </span> </p> </td> 
   <td colname="col2"> <p> 스핀 작업에 대한 두 번 클릭/탭 매핑을 구성합니다. <span class="codeph"> none </span> 으로 설정하면 두 번 클릭/탭 스핀을 사용할 수 없습니다. <span class="codeph"> 확대/축소 </span> 로 설정하면 이미지를 클릭하는 작업이 한 스핀 단계에서 회전됩니다.Ctrl 키를 누른 채로 클릭하면 한 스핀 단계가 회전됩니다. <span class="codeph"> 재설정 </span>으로 설정하면 이미지를 한 번 클릭하여 스핀을 초기 스핀 수준으로 재설정합니다. <span class="codeph"> zoomReset </span>의 경우, 현재 스핀 팩터가 지정된 제한을 초과하는 경우 재설정이 적용되며, 그렇지 않은 경우에는 스핀(spin)이 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 데스크톱 컴퓨터에서 `zoomReset` 터치 장치

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
