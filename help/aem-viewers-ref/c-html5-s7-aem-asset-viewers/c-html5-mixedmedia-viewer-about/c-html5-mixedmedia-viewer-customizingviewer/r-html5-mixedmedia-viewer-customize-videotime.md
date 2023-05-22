---
title: 비디오 시간
description: 비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 지속 시간을 보여 주는 숫자 표시입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5efae314-5f37-4afc-9b9e-3108a8529e50
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---

# 비디오 시간{#video-time}

비디오 시간은 현재 재생 중인 비디오의 현재 시간 및 지속 시간을 보여 주는 숫자 표시입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

비디오 시간 글꼴 패밀리, 글꼴 크기 및 글꼴 색상은 CSS가 제어할 수 있는 속성 중 하나입니다. 또한 CSS별로 자신을 포함하는 컨트롤 막대를 기준으로 배치할 수도 있습니다.

비디오 시간의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7videotime
```

## 비디오 시간의 CSS 속성 {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 위쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 오른쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>시간 표시 텍스트에 사용할 글꼴 색상입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

비디오 시간을 밝은 회색(16진수)으로 설정합니다. `#BBBBBB`)를 조정할 때 사용할 수 있으며, 컨트롤 막대의 위쪽에서 15픽셀, 컨트롤 막대의 오른쪽 가장자리에서 80픽셀로 크기가 조정되었습니다.

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
