---
description: 컨트롤 막대는 재생/일시 정지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에서 사용할 수 있는 모든 UI 컨트롤을 포함하고 뒤에 있는 사각형 영역입니다.
seo-description: 컨트롤 막대는 재생/일시 정지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에서 사용할 수 있는 모든 UI 컨트롤을 포함하고 뒤에 있는 사각형 영역입니다.
seo-title: 컨트롤 막대
solution: Experience Manager
title: 컨트롤 막대
topic: Dynamic media
uuid: 1fa90f7d-6b26-499d-8e6c-1cd80405aec0
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 컨트롤 막대{#control-bar}

컨트롤 막대는 재생/일시 정지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에서 사용할 수 있는 모든 UI 컨트롤을 포함하고 뒤에 있는 사각형 영역입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

컨트롤 막대는 항상 사용 가능한 전체 뷰어 너비를 사용합니다. 비디오 뷰어 컨테이너에 상대적인 색상, 높이 및 세로 위치를 CSS로 변경할 수 있습니다.

다음 CSS 클래스 선택기는 컨트롤 막대의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7controlbar
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

세로 30픽셀이고 비디오 뷰어 컨테이너의 상단에 있는 회색 컨트롤 막대로 비디오 뷰어를 설정하려면

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

