---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 06f493d7-18c9-4bb1-add6-a0dfd1a689bd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 5%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>구성 요소 미리 로드 동작을 지정합니다. <span class="codeph"> -1</span>(으)로 설정하면 구성 요소가 초기화되거나 자산이 변경될 때 모든 견본들이 동시에 로드됩니다. </p> <p><span class="codeph"> 0</span>(으)로 설정하면 보이는 견본만 로드됩니다. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>은(는) 표시되는 영역 주위에서 사전 로드되는 표시되지 않는 행/열의 수를 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`
