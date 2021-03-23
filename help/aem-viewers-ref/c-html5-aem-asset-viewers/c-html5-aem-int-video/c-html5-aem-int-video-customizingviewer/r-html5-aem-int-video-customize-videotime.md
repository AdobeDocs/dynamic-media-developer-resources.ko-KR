---
description: 비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 기간을 보여주는 숫자 표시입니다.
seo-description: 비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 기간을 보여주는 숫자 표시입니다.
seo-title: 비디오 시간
solution: Experience Manager
title: 비디오 시간
uuid: 8cec89b9-b3e8-4c58-90d9-7ab56698e35d
feature: Dynamic Media Classic,뷰어,SDK/API,대화형 비디오
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 2%

---


# 비디오 시간{#video-time}

비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 기간을 보여주는 숫자 표시입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

비디오 타임 글꼴 모음, 글꼴 크기 및 글꼴 색상은 CSS가 제어할 수 있는 속성 중 하나입니다. 또한 해당 컨트롤이 포함된 제어 막대를 기준으로 CSS로 위치를 지정할 수도 있습니다.

비디오 시간의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7videotime
```

## 비디오 시간 {#css-properties-of-video-time}의 CSS 속성

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩과 같이 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩과 같이 오른쪽 테두리에서 위치를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 비디오 시간 컨트롤의 폭입니다. 이 속성은 Internet Explorer 8 이상이 제대로 작동하려면 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>시간 표시 텍스트에 사용할 글꼴 모음입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>시간 표시 텍스트에 사용할 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>시간 표시 텍스트에 사용할 글꼴 색상입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

비디오 시간을 밝은 회색(12픽셀), 컨트롤 막대 위쪽에서 15픽셀, 컨트롤 막대의 위쪽과 오른쪽 가장자리에서 80픽셀로 설정합니다.`#BBBBBB`

```
.s7interactivevideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

