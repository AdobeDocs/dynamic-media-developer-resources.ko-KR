---
description: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,Business Practitioner
exl-id: 043196c8-63ab-439e-a28f-b76d1467f26e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-알파|gif|gif-alpha</span> </p> </td> 
   <td> <p>구성 요소가 이미지 서버에서 이미지를 로드하는 데 사용하는 이미지 형식을 지정합니다. 지정된 형식이 <span class="codeph"> -alpha</span>로 끝나는 경우 구성 요소는 이미지를 투명한 컨텐츠로 렌더링합니다. 다른 모든 이미지 형식의 경우 구성 요소는 이미지를 불투명하게 처리합니다. 구성 요소에는 기본적으로 흰색 배경이 있습니다. 따라서 백그라운드 투명화를 만들려면 <span class="codeph"> background-color</span> CSS 속성을 <span class="codeph"> transparent</span> 로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt-png-alpha`
