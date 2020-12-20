---
description: 컨트롤 막대는 재생/일시 정지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에서 사용할 수 있는 모든 사용자 인터페이스 컨트롤 뒤에 있는 사각형 영역입니다.
seo-description: 컨트롤 막대는 재생/일시 정지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에서 사용할 수 있는 모든 사용자 인터페이스 컨트롤 뒤에 있는 사각형 영역입니다.
seo-title: 컨트롤 막대
solution: Experience Manager
title: 컨트롤 막대
topic: Dynamic media
uuid: 328e34f1-9e60-4056-9a8a-e9292fb65605
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# 컨트롤 막대{#control-bar}

컨트롤 막대는 재생/일시 정지 단추, 볼륨 컨트롤 등과 같이 비디오 뷰어에서 사용할 수 있는 모든 사용자 인터페이스 컨트롤 뒤에 있는 사각형 영역입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

컨트롤 막대는 항상 사용 가능한 전체 뷰어 너비를 사용합니다. 비디오 뷰어 컨테이너를 기준으로 색상, 높이 및 수직 위치를 CSS로 변경할 수 있습니다.

다음 CSS 클래스 선택기는 컨트롤 막대의 모양을 제어합니다.

```
.s7video360viewer .s7controlbar
```

## 컨트롤 모음 {#css-properties-of-the-control-bar}의 CSS 속성

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩과 같이 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 패딩과 같이 아래쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 30픽셀의 회색 컨트롤 막대가 있고 비디오 뷰어 컨테이너의 상단에 있는 비디오 뷰어를 설정하려면

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

