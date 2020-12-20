---
description: 널
seo-description: 널
seo-title: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic media
uuid: 6fa79ce2-5191-4282-acee-5c6caad24fba
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 11%

---


# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 모든 견본에 적용되는 이미지 제공 명령 문자열. URL에 지정된 경우 <span class="codeph"> &amp;</span> 및 <span class="codeph"> = </span> 등의 모든 항목을 각각 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>으로 HTTP에서 인코딩해야 합니다. </p> <p> <p>참고: 이미지 크기 조정 조작 명령은 지원되지 않습니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

없음.

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

뷰어 URL에 지정된 경우.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정된 경우.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
