---
title: 기본 뷰어 영역
description: 기본 보기 영역은 스마트 자르기 비디오가 차지합니다. 크기를 지정하지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞게 설정됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: c8ea6698-e425-491f-8413-2260ddf40c33
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 기본 뷰어 영역{#main-viewer-area}

주요 보기 영역은 비디오가 차지합니다. 크기를 지정하지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞게 설정됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

다음 CSS 클래스 선택기는 보기 영역의 모양을 제어합니다.

```
.s7smartcropvideoviewer 
```

## 기본 뷰어 영역의 CSS 속성 {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

흰색 배경(#FFFFFF)이 있는 스마트 자르기 비디오 뷰어를 설정하고 크기를 512 x 288픽셀로 설정하려면 다음을 수행하십시오.

```
.s7smartcropvideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
