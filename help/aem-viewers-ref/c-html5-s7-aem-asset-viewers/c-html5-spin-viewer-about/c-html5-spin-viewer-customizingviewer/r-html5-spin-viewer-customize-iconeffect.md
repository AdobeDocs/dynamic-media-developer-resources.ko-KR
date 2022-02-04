---
title: 아이콘 효과
description: 스핀 표시기는 기본 뷰 영역에 겹쳐집니다. 이미지가 재설정 상태일 때 표시되고 iconeffect 매개 변수에도 따라 달라집니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 1ded69eb-62cd-49da-ab53-124348359a58
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# 아이콘 효과{#icon-effect}

스핀 표시기는 기본 뷰 영역에 겹쳐집니다. 이미지가 재설정 상태일 때 표시되고 iconeffect 매개 변수에도 따라 달라집니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7spinviewer .s7spinview .s7iconeffect
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
   <td colname="col2"> <p> 스핀 표시기 아트웍입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p>자세한 내용은 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>스핀 표시기 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>회전 표시기 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

스핀 표시기는 `state` 으로 설정된 속성 선택기 `spin_1D` 1차원 스핀 세트가 있는 경우 및 `spin_2D` 다차원 스핀 세트가 있는 경우

예 - 100 x 100픽셀 확대/축소 표시기를 설정합니다.

```
.s7spinviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```
