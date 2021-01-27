---
description: 인라인 확대/축소 모드의 기본 보기는 정적 이미지, 정적 이미지 위에 있는 플라이아웃 보기에 표시된 확대/축소 이미지, 정적 이미지 위에 표시된 팁 메시지로 구성됩니다.
seo-description: 인라인 확대/축소 모드의 기본 보기는 정적 이미지, 정적 이미지 위에 있는 플라이아웃 보기에 표시된 확대/축소 이미지, 정적 이미지 위에 표시된 팁 메시지로 구성됩니다.
seo-title: 플라이아웃 확대/축소 보기
solution: Experience Manager
title: 플라이아웃 확대/축소 보기
topic: Dynamic Media
uuid: c4c94432-7b6f-40a8-ae5f-9423234f3656
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 5%

---


# 플라이아웃 확대/축소 보기{#flyout-zoom-view}

인라인 확대/축소 모드의 기본 보기는 정적 이미지, 정적 이미지 위에 있는 플라이아웃 보기에 표시된 확대/축소 이미지, 정적 이미지 위에 표시된 팁 메시지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

기본 보기의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7flyoutzoomview
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
   <td colname="col2"> <p> 기본 보기의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 기본 보기를 투명하게 하려면 다음을 수행합니다.

```
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

팁 메시지의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

CSS를 통해 글꼴 스타일, 크기 모양 및 수직 오프셋을 구성할 수 있습니다. 그러나 가로 정렬은 뷰어 논리로 관리됩니다. `left` 또는 `right` 속성을 사용하여 CSS를 통해 덮어쓰는 것은 지원되지 않습니다.

**팁 메시지의 CSS 속성**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>메시지 배경 채우기 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> 메시지 배경 테두리 반경. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기의 아래쪽에서 오프셋합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>팁 텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 모음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도  </span> </p> </td> 
   <td colname="col2"> <p> 메시지 배경 불투명도. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 메시지 텍스트 주위에 패딩합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

팁 메시지를 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)의 현지화를 참조하십시오.

예 - 흰색 Arial 12px 글꼴과 기본 보기 아래쪽에서 50픽셀 오프셋, 패딩 및 둥근 테두리로 반투명 팁 메시지를 설정하려면 다음을 수행합니다.

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```

