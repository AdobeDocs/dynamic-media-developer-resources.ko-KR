---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,인라인 확대/축소
role: Developer,Business Practitioner
exl-id: b5b0acab-4e11-4f6a-8cb1-be6d683d7384
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 7%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 모든 견본에 적용되는 이미지 제공 명령 문자열입니다. URL에 지정된 경우 HTTP를 통해 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span>의 모든 항목을 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>로 각각 인코딩해야 합니다. </p> <p> <p>참고: 이미지 크기 조정 조작 명령은 지원되지 않습니다. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-e6310c8c4e8547689a5b48ceddb3671d}

선택 사항입니다.

## 기본값 {#section-fcb06fd8e7e945e590094efcf9a1d510}

없음.

## 예 {#section-3a188ab955c445bcb2efa3c49722c10d}

뷰어 URL에 지정된 경우.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정되는 경우입니다.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
