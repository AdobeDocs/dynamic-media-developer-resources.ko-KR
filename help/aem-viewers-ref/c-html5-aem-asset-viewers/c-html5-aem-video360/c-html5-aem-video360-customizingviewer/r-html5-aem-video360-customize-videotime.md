---
description: 비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 기간을 보여주는 숫자 표시입니다.
seo-description: 비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 기간을 보여주는 숫자 표시입니다.
seo-title: 비디오 시간
solution: Experience Manager
title: 비디오 시간
topic: Dynamic media
uuid: f8ba615f-661a-4750-bdf7-559650d464af
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 1%

---


# 비디오 시간{#video-time}

비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 기간을 보여주는 숫자 표시입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

비디오 타임 글꼴 모음, 글꼴 크기 및 글꼴 색상은 CSS가 제어할 수 있는 속성 중 하나입니다. 또한 해당 컨트롤이 포함된 제어 막대를 기준으로 CSS로 위치를 지정할 수도 있습니다.

비디오 시간의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7video360viewer .s7videotime
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

**예**  - 비디오 시간을 밝은 회색(16진수 `#BBBBBB`)으로 설정하고, 12픽셀에서 크기를 조정하며, 컨트롤 막대의 위쪽에서 15픽셀, 컨트롤 막대의 위쪽과 오른쪽 가장자리에서 80픽셀로 설정합니다.

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

