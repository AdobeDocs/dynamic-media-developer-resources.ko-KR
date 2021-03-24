---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
feature: Dynamic Media Classic,뷰어,SDK/API,혼합 미디어 집합
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 6%

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

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

없음.

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

뷰어 URL에 지정된 경우.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

구성 데이터에 지정된 경우.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
