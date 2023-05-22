---
title: ZoomView.iscommand
description: 확대/축소 이미지에 적용되는 이미지 제공 명령 문자열.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 1c24973e-1daf-4d9d-b97c-fb6a18f506ed
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# ZoomView.iscommand{#zoomview-iscommand}

확대/축소 이미지에 적용되는 이미지 제공 명령 문자열.

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> URL에 지정되는 경우 <span class="codeph"> 및</span> 및 <span class="codeph"> =</span> 은(는) (으)로 HTTP 인코딩되어야 합니다. <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>, 각각 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

없음.

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

뷰어 URL에 지정되는 경우:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정된 경우:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
