---
description: 기본 보기 영역은 비디오에 사용되고 있습니다. 일반적으로 크기를 지정하지 않으면 사용 가능한 장치 화면에 맞게 설정됩니다.
seo-description: 기본 보기 영역은 비디오에 사용되고 있습니다. 일반적으로 크기를 지정하지 않으면 사용 가능한 장치 화면에 맞게 설정됩니다.
seo-title: 기본 뷰어 영역
solution: Experience Manager
title: 기본 뷰어 영역
topic: Dynamic media
uuid: f395b22d-55b8-4422-9aa4-9dd4b7a24063
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---


# 기본 뷰어 영역{#main-viewer-area}

기본 보기 영역은 비디오에 사용되고 있습니다. 일반적으로 크기를 지정하지 않으면 사용 가능한 장치 화면에 맞게 설정됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

다음 CSS 클래스 선택기는 보기 영역의 모양을 제어합니다.

```
.s7videoviewer 
```

## 기본 뷰어 영역 {#css-properties-of-the-main-viewer-area}의 CSS 속성

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>뷰어 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>뷰어 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 16진수 형식의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

흰색 배경(#FFFFFF)을 사용하여 비디오 뷰어를 설정하고 크기를 512 x 288픽셀로 설정하려면:

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

