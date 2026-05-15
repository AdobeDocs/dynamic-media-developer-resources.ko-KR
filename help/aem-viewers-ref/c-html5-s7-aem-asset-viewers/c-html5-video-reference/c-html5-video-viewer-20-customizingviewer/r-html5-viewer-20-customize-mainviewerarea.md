---
title: 기본 뷰어 영역
description: 주요 보기 영역은 비디오가 차지합니다. 크기를 지정하지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞게 설정됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 7d1379c1-7746-4f61-92df-e8ac4ab7d506
TQID: 'https://experienceleague.adobe.com/n6O9ImN-hYhsVOclN9zrI6fT4gd0gBpRhewmrzCOTSE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# 기본 뷰어 영역{#main-viewer-area}

주요 보기 영역은 비디오가 차지합니다. 크기를 지정하지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞게 설정됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

다음 CSS 클래스 선택기는 보기 영역의 모양을 제어합니다.

```
.s7videoviewer 
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

흰색 배경(#FFFFFF)이 있는 비디오 뷰어를 설정하고 크기를 512 x 288픽셀로 설정하려면 다음 작업을 수행하십시오.

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
