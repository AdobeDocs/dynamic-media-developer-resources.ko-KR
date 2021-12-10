---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---

# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadbr</span></span> </p> </td> 
   <td colname="col2"> <p>구성 요소 사전 로드 동작을 지정합니다. </p> <p>로 설정된 경우 <span class="codeph"> -1</span> 구성 요소는 유휴 상태일 때 모든 카탈로그 프레임을 미리 로드합니다. </p> <p> 로 설정된 경우 <span class="codeph"> 0</span> 구성 요소는 현재 표시된 프레임, 이전 프레임 및 다음 프레임만 로드합니다. </p> <p>설정 <span class="codeph"><span class="varname"> preloadbr</span></span> 유휴 상태에서 현재 표시된 프레임 주위의 보이지 않는 프레임 수를 정의하는 데 사용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-4b7952997f9240e581d21bcdb173f9af}

선택 사항입니다.

## 기본값 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## 예 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
