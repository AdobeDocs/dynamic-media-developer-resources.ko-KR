---
title: SpinView.iscommand
description: SpinView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: d616c8cf-6717-48f9-9926-1b37afe0e444
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> 스핀 이미지에 적용되는 이미지 제공 명령 문자열입니다. URL에 지정된 경우 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span> 는 HTTP로 인코딩되어야 합니다. <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>각각 입니다. </p> <p> <p>참고: 이미지 크기 조정 조작 명령은 지원되지 않습니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

없음.

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

뷰어 URL에 지정된 경우:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정되는 경우:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
