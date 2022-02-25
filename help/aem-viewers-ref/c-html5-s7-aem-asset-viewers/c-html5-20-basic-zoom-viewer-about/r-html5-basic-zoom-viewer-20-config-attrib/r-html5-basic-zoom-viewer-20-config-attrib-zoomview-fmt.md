---
title: ZoomView.fmt
description: ZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 7cb75d38-a577-4e06-b679-c4e00db5059a
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-알파|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 구성 요소가 이미지 서버에서 이미지를 로드하는 데 사용하는 이미지 형식을 지정합니다. 지정된 형식이 "-alpha"로 끝나는 경우 구성 요소는 이미지를 투명한 컨텐츠로 렌더링합니다. 다른 모든 이미지 형식의 경우 구성 요소는 이미지를 불투명하게 처리합니다. 구성 요소에는 기본적으로 흰색 배경이 있습니다. 따라서 투명하도록 하려면 배경색 CSS 속성을 투명으로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-50bcd15223174bb79ce08b31ea03d682}

선택 사항입니다.

## 기본값 {#section-7564169749ff4a4996049ea1148cb2a5}

`jpeg`

## 예 {#section-96e69b70365f461dae4399e49044ea2f}

`fmt=png-alpha`
