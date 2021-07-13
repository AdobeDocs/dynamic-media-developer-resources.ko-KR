---
description: 컨트롤 막대는 재생/일시 정지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에 사용할 수 있는 모든 UI 컨트롤을 포함하고 있는 사각형 영역입니다.
solution: Experience Manager
title: 컨트롤 막대
feature: Dynamic Media Classic,Viewers,SDK/API,비디오
role: Developer,User
exl-id: 2239307a-4a05-4392-b35c-a64ea6c938ad
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---

# 컨트롤 막대{#control-bar}

컨트롤 막대는 재생/일시 정지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에 사용할 수 있는 모든 UI 컨트롤을 포함하고 있는 사각형 영역입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

컨트롤 막대는 항상 사용 가능한 전체 뷰어 너비를 사용합니다. 비디오 뷰어 컨테이너를 기준으로 색상, 높이 및 세로 위치를 CSS로 변경할 수 있습니다.

다음 CSS 클래스 선택기는 컨트롤 막대의 모양을 제어합니다.

```
.s7videoviewer .s7controlbar
```

## 컨트롤 막대의 CSS 속성 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 아래쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
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

30픽셀이고 비디오 뷰어 컨테이너의 맨 위에 있는 회색 컨트롤 막대가 있는 비디오 뷰어를 설정하려면 다음을 수행하십시오.

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
