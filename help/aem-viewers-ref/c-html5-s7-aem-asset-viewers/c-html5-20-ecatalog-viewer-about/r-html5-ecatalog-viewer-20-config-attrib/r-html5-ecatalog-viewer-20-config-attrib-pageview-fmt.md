---
title: PageView.fmt
description: PageView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 07aec907-fb9d-41c8-9f32-a4886605db35
source-git-commit: 5432393e265fba888579d700cf2f414dc4f680af
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 구성 요소가 이미지 서버에서 이미지를 로드하는 데 사용하는 이미지 형식을 지정합니다. 지정된 형식이 다음으로 끝나는 경우 <span class="codeph"> -알파</span>, 구성 요소는 이미지를 투명한 콘텐츠로 렌더링합니다. 기타 모든 이미지 형식의 경우 구성 요소는 이미지를 불투명한 것으로 처리합니다. 구성 요소에는 기본적으로 흰색 배경이 있습니다. 따라서 투명하게 하려면 다음을 설정하십시오. <span class="codeph"> background-color</span> CSS 속성 대상 <span class="codeph"> 투명</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

선택적.

## 기본값 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## 예 {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
