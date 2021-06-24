---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>구성 요소 사전 로드 동작을 지정합니다. </p> <p><span class="codeph"> -1</span>로 설정하면 유휴 상태이면 구성 요소가 모든 카탈로그 프레임을 미리 로드합니다. </p> <p> <span class="codeph"> 0</span> 로 설정하면 구성 요소는 현재 표시된 프레임, 이전 프레임 및 다음 프레임만 로드합니다. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> 을 설정하여 현재 표시된 프레임 주위에 표시되는 보이지 않는 프레임이 유휴 상태로 사전 로드되는 횟수를 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-4b7952997f9240e581d21bcdb173f9af}

선택 사항입니다.

## 기본값 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 예 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
