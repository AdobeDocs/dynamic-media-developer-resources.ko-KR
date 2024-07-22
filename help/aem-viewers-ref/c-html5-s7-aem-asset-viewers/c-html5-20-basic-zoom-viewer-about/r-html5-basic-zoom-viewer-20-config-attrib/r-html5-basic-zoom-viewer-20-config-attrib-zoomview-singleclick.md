---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c2292b5b-5b4e-4368-9495-9108042ec2f1
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소 재설정 </span> </p> </td> 
   <td colname="col2"> <p> 한 번 클릭/누르기로 확대/축소하는 동작의 매핑을 구성합니다. <span class="codeph"> 없음 </span>(으)로 설정하면 한 번 클릭/탭 확대/축소가 비활성화됩니다. <span class="codeph"> 확대/축소로 설정된 경우 </span> 이미지를 클릭하면 1단계 확대되고, Ctrl 키를 누른 상태에서 클릭하면 1단계 축소됩니다. <span class="codeph"> 재설정 </span>(으)로 설정하면 이미지를 한 번 클릭할 때 확대/축소가 초기 확대/축소 수준으로 재설정됩니다. <span class="codeph"> zoomReset </span>의 경우 현재 확대/축소 비율이 지정된 제한에 도달하거나 초과할 경우 재설정이 적용되며 그렇지 않으면 확대/축소가 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-50bcd15223174bb79ce08b31ea03d682}

선택적.

## 기본값 {#section-7564169749ff4a4996049ea1148cb2a5}

데스크톱 컴퓨터에서는 `zoomReset`, 터치 장치에서는 `none`입니다.

## 예 {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
