---
title: 회전 보기 아이콘 효과
description: 스핀 표시기가 스핀 보기 영역 위에 오버레이됩니다. 이미지가 재설정 상태일 때 표시되며, 이는 iconeffect 매개 변수에도 의존합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1c5c73f9-c32a-4bca-93f0-c5a95756355b
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# 회전 보기 아이콘 효과{#spin-view-icon-effect}

스핀 표시기가 스핀 보기 영역 위에 오버레이됩니다. 이미지가 재설정 상태일 때 표시되며, 이는 iconeffect 매개 변수에도 의존합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 보기 영역의 모양이 제어됩니다.

```
.s7mixedmediaviewer .s7spinview .s7iconeffect
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 회전 표시기 아트워크입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>회전 표시기 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>회전 표시기 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

회전 표시기는 1차원 회전 집합이 있는 경우 `spin_1D`(으)로 설정되고 다차원 회전 집합이 있는 경우 `spin_2D`(으)로 설정된 `state` 특성 선택기를 지원합니다.

예 - 100x100픽셀 확대/축소 표시기를 설정합니다.

```
.s7mixedmediaviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```
