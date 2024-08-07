---
title: PanoramicView.fmt
description: 구성 요소가 이미지 서버에서 이미지를 로드하는 데 사용하는 이미지 형식을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

구성 요소가 이미지 서버에서 이미지를 로드하는 데 사용하는 이미지 형식을 지정합니다. 지정된 형식이 &quot;-alpha&quot;로 끝날 경우, 구성 요소는 이미지를 투명한 것으로 렌더링합니다. 기타 모든 이미지 형식의 경우 구성 요소는 이미지를 불투명한 것으로 처리합니다. 구성 요소에는 기본적으로 투명한 배경이 있습니다. 따라서 불투명하게 하려면 `background-color` CSS 속성을 `desired_color`(으)로 설정하십시오.

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> 이미지 서버에서 이미지를 로드하기 위해 구성 요소에서 사용할 이미지 형식을 지정합니다. 지정된 형식이 "-alpha"로 끝날 경우, 구성 요소는 이미지를 투명한 컨텐츠로 렌더링합니다. 기타 모든 이미지 형식의 경우 구성 요소는 이미지를 불투명한 것으로 처리합니다. 구성 요소에는 기본적으로 투명한 배경이 있습니다. 따라서 불투명하게 하려면 background-color CSS 속성을 원하는 색상으로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
