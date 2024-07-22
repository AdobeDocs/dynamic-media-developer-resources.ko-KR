---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 690aed79-c242-402d-86c0-470a91fbb034
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# PageView.fmt{#pageview-fmt}

[!DNL `[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 구성 요소가 이미지 서버에서 이미지를 로드하는 데 사용하는 이미지 형식을 지정합니다. 지정된 형식이 <span class="codeph"> -alpha</span>(으)로 끝날 경우, 구성 요소는 이미지를 투명한 컨텐츠로 렌더링합니다. 기타 모든 이미지 형식의 경우 구성 요소는 이미지를 불투명한 것으로 처리합니다. 구성 요소에는 기본적으로 흰색 배경이 있습니다. 따라서 투명하게 하려면 <span class="codeph"> background-color</span> CSS 속성을 <span class="codeph"> transparent</span>(으)로 설정하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

선택적.

## 기본값 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## 예 {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
