---
title: 플라이아웃 확대/축소 보기
description: 기본 보기는 정적 이미지 위에 있는 플라이아웃 보기에 표시되는 정적 이미지와 확대/축소된 이미지로 구성됩니다. 또한 정적 이미지 위에 표시되는 팁 메시지로 구성됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# 플라이아웃 확대/축소 보기{#flyout-zoom-view}

기본 보기는 정적 이미지 위에 있는 플라이아웃 보기에 표시되는 정적 이미지와 확대/축소된 이미지로 구성됩니다. 또한 정적 이미지 위에 표시되는 팁 메시지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

기본 보기의 **CSS 속성**

기본 보기의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 기본 보기를 투명하게 하려면 다음을 수행합니다.

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

팁 메시지의 **CSS 속성**

팁 메시지의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

CSS를 통해 폰트 스타일, 크기, 모양, 수직 옵셋 등을 구성할 수 있다. 그러나 수평 정렬은 뷰어 논리에 의해 관리됩니다. `left` 또는 `right` 속성을 사용하여 CSS를 통해 재정의할 수 없습니다.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>기본 뷰의 아래쪽에서 오프셋합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트 주위에 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트의 배경 채우기 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트의 배경 테두리 반경. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도 </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트의 배경 불투명도입니다. </p> <p>Internet Explorer 8의 경우 <span class="codeph"> filter:alpha(opacity-...) ) </span> 사용 </p> </td> 
  </tr> 
 </tbody> 
</table>

팁 메시지는 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27)를 참조하십시오.

.

예 - 흰색 Arial® 12px 글꼴, 기본 보기 아래쪽에서 오프셋된 50픽셀, 패딩 및 둥글게 표시된 테두리를 사용하여 반투명 팁 메시지를 설정하려면 다음 작업을 수행하십시오.

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
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
