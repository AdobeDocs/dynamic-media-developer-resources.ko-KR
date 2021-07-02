---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,Business Practitioner
exl-id: e87981f8-8174-432a-89ea-fae74d0584ad
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

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

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 데스크톱 컴퓨터에서 `zoomReset` 터치 장치

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
