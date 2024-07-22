---
title: SpinView.fmt
description: SpinView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4bb6c242-9f1a-440f-9fca-bf26e66e4114
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_68C0C3D5C60640DC9A8EE04EA685AB99"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 구성 요소가 이미지 서버에서 이미지를 로드하는 데 사용하는 이미지 형식을 지정합니다. 지정된 형식이 <span class="codeph"> -alpha</span>(으)로 끝날 경우, 구성 요소는 이미지를 투명한 컨텐츠로 렌더링합니다. 기타 모든 이미지 형식의 경우 구성 요소는 이미지를 불투명한 것으로 처리합니다. </p> <p>구성 요소에는 기본적으로 흰색 배경이 있습니다. 따라서 투명하게 하려면 <span class="codeph"> background-color</span> CSS 속성을 <span class="codeph"> transparent</span>(으)로 설정하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
