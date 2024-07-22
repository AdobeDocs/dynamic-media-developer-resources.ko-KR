---
title: 컨트롤 막대
description: 컨트롤 막대는 재생/일시 중지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에서 사용할 수 있는 모든 사용자 인터페이스 컨트롤을 포함하고 뒤에 있는 사각형 영역입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# 컨트롤 막대{#control-bar}

컨트롤 막대는 재생/일시 중지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에서 사용할 수 있는 모든 사용자 인터페이스 컨트롤을 포함하고 뒤에 있는 사각형 영역입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

컨트롤 막대는 항상 사용 가능한 전체 뷰어 너비를 사용합니다. 비디오 뷰어 컨테이너를 기준으로 CSS별로 색상, 높이 및 세로 위치를 변경할 수 있습니다.

다음 CSS 클래스 선택기는 컨트롤 막대의 모양을 제어합니다.

```
.s7mixedmediaviewer .s7controlbar
```

## 컨트롤 막대의 CSS 속성 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

30픽셀 높이의 회색 컨트롤 막대가 있는 혼합 미디어 뷰어를 설정합니다.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
