---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소재설정 </span> </p> </td> 
   <td colname="col2"> <p> 확대/축소 작업을 위한 단일 클릭/탭 매핑을 구성합니다. 설정 대상 <span class="codeph"> 없음 </span> 단일 클릭/탭 확대/축소를 비활성화합니다. 로 설정된 경우 <span class="codeph"> 확대/축소 </span> 이미지를 한 확대/축소 단계로 확대/축소합니다. Ctrl 키를 누른 상태에서 클릭하여 한 확대/축소 단계를 축소합니다. 설정 대상 <span class="codeph"> 재설정 </span> 이미지를 한 번 클릭하면 확대/축소가 초기 확대/축소 수준으로 재설정됩니다. 대상 <span class="codeph"> zoomReset </span>, 현재 확대/축소 비율이 지정된 제한 이상인 경우 재설정이 적용되고, 그렇지 않은 경우 확대/축소가 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`zoomReset` - 데스크탑 컴퓨터 `none` 터치 장치

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
