---
title: 비디오 시간
description: 비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 기간을 표시하는 숫자 표시입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 78657fd2-e805-4047-be0a-592143025986
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 비디오 시간{#video-time}

비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 기간을 표시하는 숫자 표시입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

비디오 시간 글꼴 패밀리, 글꼴 크기 및 글꼴 색상은 CSS에서 제어할 수 있는 속성 중 하나입니다. 또한 이 위치를 해당 컨트롤을 포함하는 컨트롤 막대를 기준으로 CSS로 배치할 수도 있습니다.

비디오 시간의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7video360viewer .s7videotime
```

## 비디오 시간의 CSS 속성 {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 오른쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 비디오 시간 제어의 폭입니다. 이 속성은 Internet Explorer 8 이상이 제대로 작동하려면 필요합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>시간 표시 텍스트에 사용할 글꼴 모음입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>시간 표시 텍스트에 사용할 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>시간 표시 텍스트에 사용할 글꼴 색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 비디오 시간을 12픽셀로, 컨트롤 막대의 상단에서 15픽셀로, 컨트롤 막대의 상단과 오른쪽 모서리에서 80픽셀로 설정합니다(16진수 `#BBBBBB`).

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
