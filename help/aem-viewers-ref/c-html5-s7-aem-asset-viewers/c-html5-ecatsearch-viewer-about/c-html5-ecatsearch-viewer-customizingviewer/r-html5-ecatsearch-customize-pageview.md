---
title: 페이지 보기
description: 기본 보기는 카탈로그 이미지로 구성됩니다. 다른 페이지로 이동하거나 확대/축소할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 3%

---

# 페이지 보기{#page-view}

기본 보기는 카탈로그 이미지로 구성됩니다. 다른 페이지로 이동하거나 확대/축소할 수 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 보기 영역의 모양이 제어됩니다.

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 16진수 형식의 기본 보기의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 커서 </span> </p> </td> 
   <td colname="col2"> <p>기본 보기에 표시되는 커서입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 기본 보기를 투명하게 합니다.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

데스크탑 시스템에서 구성 요소는 `cursortype` 적용할 수 있는 속성 선택기 `.s7pageview` 클래스 및 컨트롤은 구성 요소 상태 및 사용자 작업을 기반으로 커서의 형식을 제어합니다. 다음 `cursortype` 값이 지원됩니다.

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>값 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 기본값 </span> </p> </td> 
   <td colname="col2"> <p>작은 이미지 해상도, 구성 요소 설정 또는 둘 다로 인해 이미지를 확대/축소할 수 없을 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>이미지를 확대할 수 있을 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 재설정 </span> </p> </td> 
   <td colname="col2"> <p>이미지가 최대 확대/축소 레벨에 있고 초기 상태로 재설정할 수 있을 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 드래그 </span> </p> </td> 
   <td colname="col2"> <p>사용자가 확대 중인 이미지를 패닝할 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 슬라이드 </span> </p> </td> 
   <td colname="col2"> <p>사용자가 가로 스와이프 또는 긋기를 수행하여 이미지 교체를 수행할 때 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

카탈로그 스프레드의 왼쪽 페이지와 오른쪽 페이지를 시각적으로 구분하는 페이지 구분선은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 페이지 구분선의 폭입니다. 다음으로 설정 <span class="codeph"> 0 </span> 구분선을 완전히 숨기려면 px를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>페이지 구분선으로 사용할 이미지입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 반투명 이미지가 있는 40픽셀 폭의 페이지 구분선을 사용합니다.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>다음의 경우 `frametransition` 수정자가 다음으로 설정됨 `turn` 또는 `auto` (데스크탑 시스템에서는) 페이지 구분선의 모양이 `pageturnstyle` 수정자 및 `.s7pagedivider` CSS 클래스는 무시됩니다.

기본 뷰어 영역 위에 사용자 지정 마우스 커서를 표시하도록 구성할 수 있습니다. 이 기능은에 적용되는 추가 속성 선택기로 제어됩니다 `.s7ecatalogsearchviewer .s7pageview` CSS 클래스:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 기본값 </span> </p> </td> 
   <td colname="col2"> <p> 일반적으로 화살표는 확대/축소할 수 없는 이미지에 대해 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> 이미지를 확대할 수 있는 시기를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 재설정 </span> </p> </td> 
   <td colname="col2"> <p>이미지가 최대 확대/축소이고 재설정될 수 있는 시기를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 드래그 </span> </p> </td> 
   <td colname="col2"> <p>사용자가 확대 이미지에 대한 드래그 작업을 수행할 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 슬라이드 </span> </p> </td> 
   <td colname="col2"> <p>사용자가 슬라이드 제스처를 사용하여 이미지 교환을 수행하는 경우 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 구성 요소 상태 유형마다 다른 마우스 커서를 사용합니다.

```
.s7ecatalogsearchviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
