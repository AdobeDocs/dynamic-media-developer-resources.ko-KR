---
title: ZoomView.fmt
description: 구성 요소가 이미지 서버에서 이미지를 로드하는 데 사용하는 이미지 형식을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 6a023abb-71c7-4db5-8d05-bf0a4b1fc3a0
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# ZoomView.fmt{#zoomview-fmt}

구성 요소가 이미지 서버에서 이미지를 로드하는 데 사용하는 이미지 형식을 지정합니다.

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 지정된 형식이 다음으로 끝나는 경우 <span class="codeph"> -알파</span>, 구성 요소는 이미지를 투명한 콘텐츠로 렌더링합니다. 기타 모든 이미지 형식의 경우 구성 요소는 이미지를 불투명한 것으로 처리합니다. 구성 요소에는 기본적으로 흰색 배경이 있습니다. 따라서 투명하게 하려면 다음을 설정하십시오. <span class="codeph"> background-color</span> CSS 속성 대상 <span class="codeph"> 투명</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
