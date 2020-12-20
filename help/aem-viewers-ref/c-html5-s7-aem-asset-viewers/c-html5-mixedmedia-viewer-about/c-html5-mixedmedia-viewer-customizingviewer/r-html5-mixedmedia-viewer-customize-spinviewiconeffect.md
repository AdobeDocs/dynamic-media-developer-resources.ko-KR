---
description: 회전 표시기는 회전 보기 영역에 오버레이됩니다. 이미지가 재설정 상태일 때 표시되며 iconeffect 매개 변수도 다릅니다.
seo-description: 회전 표시기는 회전 보기 영역에 오버레이됩니다. 이미지가 재설정 상태일 때 표시되며 iconeffect 매개 변수도 다릅니다.
seo-title: 회전 보기 아이콘 효과
solution: Experience Manager
title: 회전 보기 아이콘 효과
topic: Dynamic media
uuid: 33445a3d-51dc-47a4-a8d1-87d25ea001e1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# 회전 보기 아이콘 효과{#spin-view-icon-effect}

회전 표시기는 회전 보기 영역에 오버레이됩니다. 이미지가 재설정 상태일 때 표시되며 iconeffect 매개 변수도 다릅니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> 회전 표시기 아트웍입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS 스프라이트 </a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>회전 표시기 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>회전 표시기 높이. </p> </td> 
  </tr> 
 </tbody> 
</table>

스핀 표시기는 1차원 스핀 세트의 경우 `spin_1D`, 다차원 스핀 세트의 경우 `spin_2D`로 설정된 `state` 속성 선택기를 지원합니다.

예 - 100 x 100픽셀 확대/축소 표시기를 설정하려면

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

