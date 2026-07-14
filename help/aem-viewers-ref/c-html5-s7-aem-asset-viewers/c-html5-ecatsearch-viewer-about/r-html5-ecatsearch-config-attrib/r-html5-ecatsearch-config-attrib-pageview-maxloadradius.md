---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cf769b2d-be4e-4d93-9620-00a438157693
TQID: 'https://experienceleague.adobe.com/sknjvd6z4eMeDsDiUTdPT8KjOBdYEWEahgp9bbyq8V4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>구성 요소 미리 로드 동작을 지정합니다. </p> <p><span class="codeph"> -1</span>(으)로 설정된 경우 구성 요소가 유휴 상태일 때 모든 카탈로그 프레임을 미리 로드합니다. </p> <p> <span class="codeph"> 0</span>(으)로 설정하면 구성 요소가 표시되는 프레임, 이전 프레임 및 다음 프레임만 로드합니다. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>을(를) 설정하여 유휴 상태에서 현재 표시된 프레임 주위에 있는 보이지 않는 프레임을 얼마나 미리 로드할지를 정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-4b7952997f9240e581d21bcdb173f9af}

선택적.

## 기본값 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## 예 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
