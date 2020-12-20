---
description: 널
seo-description: 널
seo-title: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
topic: Dynamic media
uuid: 2f44dc7f-ebed-4c74-b1ea-0b65655059fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|확대/축소|재설정|확대/축소 재설정  </span> </p> </td> 
   <td colname="col2"> <p> 확대/축소 작업에 대한 두 번 클릭/탭 매핑을 구성합니다. <span class="codeph"> none </span>으로 설정하면 확대/축소를 두 번 클릭/탭할 수 없습니다. <span class="codeph"> 확대/축소 </span>로 설정된 경우 이미지를 클릭하면 한 확대/축소 단계로 확대/축소됩니다.Ctrl 키를 누른 상태에서 클릭하여 한 단계 확대/축소 <span class="codeph"> 재설정 </span>으로 설정하면 이미지를 한 번 클릭하면 확대/축소 레벨이 초기 확대/축소 수준으로 재설정됩니다. <span class="codeph"> zoomReset </span>의 경우 현재 확대/축소 요소가 지정된 제한 범위 내에 있거나 그 범위를 초과하는 경우 재설정이 적용되며, 그렇지 않은 경우 확대/축소가 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 데스크톱 컴퓨터에; `zoomReset` 터치 디바이스에서 사용

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
