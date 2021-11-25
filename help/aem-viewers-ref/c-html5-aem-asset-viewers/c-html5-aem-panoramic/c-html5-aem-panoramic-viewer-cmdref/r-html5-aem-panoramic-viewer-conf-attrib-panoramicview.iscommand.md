---
title: PanoramicView.iscommand
description: 파노라마 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 2726733691296fb86b0022ac61ac654848fe83cf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

파노라마 뷰어에 대한 구성 속성입니다.

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 이미지에 적용되는 이미지 제공 명령 문자열입니다.  URL에 지정된 경우 모든 항목을 HTTP로 인코딩해야 합니다 <span class="codeph"> &amp;</span> 및 <span class="codeph"> =</span> 로서의 <span class="codeph"> %26</span> 및 <span class="codeph"> %3D</span>각각 입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>


## 속성 {#section-f42369774e2740dcb399626a0e4e930e}

선택 사항입니다.

## 기본값 {#section-d016470e92a74f98a18c4ab3489410a5}

기본값은 없습니다.

## 예 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

뷰어 URL에 지정된 경우.

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

구성 데이터에 지정되는 경우.

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
