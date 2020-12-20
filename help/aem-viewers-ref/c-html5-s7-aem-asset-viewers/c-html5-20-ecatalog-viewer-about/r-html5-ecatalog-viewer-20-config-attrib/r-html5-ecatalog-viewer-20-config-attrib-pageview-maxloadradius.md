---
description: 널
seo-description: 널
seo-title: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
topic: Dynamic media
uuid: 425624c5-3cbe-4b63-8c6b-eff31f2ed919
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 8%

---


# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>구성 요소 미리 로드 동작을 지정합니다. </p> <p><span class="codeph"> -1</span>으로 설정하면 구성 요소가 유휴 상태일 때 모든 카탈로그 프레임을 미리 로드합니다. </p> <p> <span class="codeph"> 0</span>으로 설정하면 구성 요소는 현재 표시된 프레임, 이전 프레임 및 다음 프레임만 로드합니다. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> 을 설정하여 현재 표시된 프레임 주위에 유휴 상태로 미리 로드되는 보이지 않는 프레임 수를 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-4b7952997f9240e581d21bcdb173f9af}

선택 사항입니다.

## 기본값 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 예 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
