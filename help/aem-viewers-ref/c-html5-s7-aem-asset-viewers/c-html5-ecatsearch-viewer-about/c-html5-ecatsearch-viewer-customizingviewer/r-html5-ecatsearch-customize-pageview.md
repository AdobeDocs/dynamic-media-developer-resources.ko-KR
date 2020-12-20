---
description: 기본 보기는 카탈로그 이미지로 구성됩니다. 다른 페이지로 이동하거나 확대하기 위해 스와이프할 수 있습니다.
seo-description: 기본 보기는 카탈로그 이미지로 구성됩니다. 다른 페이지로 이동하거나 확대하기 위해 스와이프할 수 있습니다.
seo-title: 페이지 보기
solution: Experience Manager
title: 페이지 보기
topic: Dynamic media
uuid: f585bf57-c66a-4213-a2af-d9625beb5bed
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 2%

---


# 페이지 보기{#page-view}

기본 보기는 카탈로그 이미지로 구성됩니다. 다른 페이지로 이동하거나 확대하기 위해 스와이프할 수 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 16진수 형식의 기본 보기의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 커서  </span> </p> </td> 
   <td colname="col2"> <p>기본 보기 위에 표시되는 커서입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 기본 보기를 투명하게 만듭니다.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

데스크톱 시스템에서 구성 요소는 `cursortype` 속성 선택기를 지원하며 구성 요소 상태 및 사용자 작업을 기반으로 커서의 유형을 제어합니다. `.s7pageview` 다음 `cursortype` 값이 지원됩니다.

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
   <td colname="col2"> <p>작은 이미지 해상도, 구성 요소 설정 또는 둘 다로 인해 이미지를 확대할 수 없을 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoom  </span> </p> </td> 
   <td colname="col2"> <p>이미지를 확대할 수 있을 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 재설정 </span> </p> </td> 
   <td colname="col2"> <p>이미지가 최대 확대/축소 수준에 있을 때 표시되며 초기 상태로 재설정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 드래그 </span> </p> </td> 
   <td colname="col2"> <p>사용자가 확대 상태의 이미지를 이동할 때 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide  </span> </p> </td> 
   <td colname="col2"> <p>사용자가 가로로 스와이프 또는 터치를 수행하여 이미지 교환을 수행할 때 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

카탈로그 스프레드의 왼쪽 및 오른쪽 페이지를 시각적으로 구분하는 페이지 구분선은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col2"> <p> 페이지 구분선의 폭입니다. 분할자를 완전히 숨기려면 <span class="codeph"> 0 </span> px로 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>페이지 구분선으로 사용할 이미지입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 반투명 이미지와 40픽셀 너비의 페이지 구분선을 갖습니다.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>`frametransition` 수정자가 `turn` 또는 `auto`(데스크탑 시스템)으로 설정된 경우 페이지 구분자의 모양은 `pageturnstyle` 수정자로 제어되고 `.s7pagedivider` CSS 클래스는 무시됩니다.

주 뷰어 영역 위에 사용자 정의 마우스 커서를 표시할 수 있습니다. 이것은 `.s7ecatalogsearchviewer .s7pageview` CSS 클래스에 적용된 추가 속성 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> zoom  </span> </p> </td> 
   <td colname="col2"> <p> 이미지를 확대할 수 있는 시기를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 재설정 </span> </p> </td> 
   <td colname="col2"> <p>이미지를 최대 확대/축소 크기로 설정하고 재설정할 수 있는 시기를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 드래그 </span> </p> </td> 
   <td colname="col2"> <p>사용자가 확대된 이미지에서 드래그 작업을 수행하는 시기를 표시합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide  </span> </p> </td> 
   <td colname="col2"> <p>사용자가 슬라이드 제스처를 사용하여 이미지 교환을 수행하는 시기를 표시합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 각 구성 요소 상태 유형에 대해 서로 다른 마우스 커서를 갖습니다.

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

