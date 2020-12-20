---
description: 널
seo-description: 널
seo-title: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic media
uuid: 42327f03-269b-4d4e-a35d-2537ca3ba071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소 재설정  </span> </p> </td> 
   <td colname="col2"> <p> 한 번 클릭/탭으로 확대/축소 동작 매핑을 구성합니다.<span class="codeph"> none </span>으로 설정하면 한 번의 클릭/탭 확대/축소가 비활성화됩니다. <span class="codeph"> 확대/축소 </span>로 설정된 경우 이미지를 클릭하면 한 확대/축소 단계로 확대/축소됩니다.Ctrl 키를 누른 상태에서 클릭하여 한 단계 확대/축소 <span class="codeph"> 재설정 </span>으로 설정하면 이미지를 한 번 클릭하면 확대/축소 레벨이 초기 확대/축소 수준으로 재설정됩니다. <span class="codeph"> zoomReset </span>의 경우 현재 확대/축소 요소가 지정된 제한 범위 내에 있거나 그 범위를 초과하는 경우 재설정이 적용되며, 그렇지 않은 경우 확대/축소가 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-50bcd15223174bb79ce08b31ea03d682}

선택 사항입니다.

## 기본값 {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` 데스크톱 컴퓨터에; `none` 터치 디바이스에서 사용

## 예 {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
