---
title: 비디오 시간
description: 비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 지속 시간을 보여 주는 숫자 표시입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0ef09f06-c2d5-4c84-8ff9-4e94e9e54d40
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# 비디오 시간{#video-time}

비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 지속 시간을 보여 주는 숫자 표시입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

비디오 시간 글꼴 패밀리, 글꼴 크기 및 글꼴 색상은 CSS가 제어할 수 있는 속성 중 하나입니다. 또한 CSS별로 자신을 포함하는 컨트롤 막대를 기준으로 배치할 수도 있습니다.

비디오 시간의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7smartcropvideoviewer .s7videotime
```

## 비디오 시간의 CSS 속성 {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 위쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 오른쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 비디오 시간 컨트롤의 폭입니다. Internet Explorer 8 이상이 제대로 작동하려면 이 속성이 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>시간에 사용할 글꼴 모음 표시 텍스트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>시간 표시 텍스트에 사용할 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p>시간 표시 텍스트에 사용할 글꼴 색상입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

비디오 시간을 밝은 회색(16진수 `#BBBBBB`)으로 설정합니다. 이 값은 12픽셀이며 컨트롤 막대의 맨 위에서 15픽셀, 컨트롤 막대의 오른쪽 가장자리에서 80픽셀입니다.

```
.s7smartcropvideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
