---
description: SearchPanel.fmt
solution: Experience Manager
title: SearchPanel.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog 검색
role: Developer,Business Practitioner
exl-id: a713b8f1-e834-457d-b038-eb30b25f905f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# SearchPanel.fmt{#searchpanel-fmt}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-알파|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 구성 요소가 이미지 서버에서 이미지를 로드하는 데 사용하는 이미지 형식을 지정합니다. 이미지 서버와 클라이언트 브라우저에서 지원하는 모든 형식일 수 있습니다. </p> <p>지정된 형식이 <span class="codeph"> -alpha</span>로 끝나는 경우 구성 요소는 이미지를 투명한 컨텐츠로 렌더링합니다. 다른 모든 이미지 형식의 경우 구성 요소는 이미지를 불투명하게 처리합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

선택 사항입니다.

## 기본값 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## 예 {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
