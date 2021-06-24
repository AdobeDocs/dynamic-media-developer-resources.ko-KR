---
description: 컨트롤 막대는 재생/일시 정지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에 사용할 수 있는 모든 사용자 인터페이스 컨트롤을 포함하고 있는 사각형 영역입니다.
solution: Experience Manager
title: 컨트롤 막대
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,Business Practitioner
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# 컨트롤 막대{#control-bar}

컨트롤 막대는 재생/일시 정지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에 사용할 수 있는 모든 사용자 인터페이스 컨트롤을 포함하고 있는 사각형 영역입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

컨트롤 막대는 항상 사용 가능한 전체 뷰어 너비를 사용합니다. 비디오 뷰어 컨테이너를 기준으로 색상, 높이 및 세로 위치를 CSS로 변경할 수 있습니다.

다음 CSS 클래스 선택기는 컨트롤 막대의 모양을 제어합니다.

```
.s7mixedmediaviewer .s7controlbar
```

## 컨트롤 막대의 CSS 속성 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

30픽셀 높이의 회색 컨트롤 막대가 있는 혼합 미디어 뷰어를 설정하려면 다음을 수행합니다.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
