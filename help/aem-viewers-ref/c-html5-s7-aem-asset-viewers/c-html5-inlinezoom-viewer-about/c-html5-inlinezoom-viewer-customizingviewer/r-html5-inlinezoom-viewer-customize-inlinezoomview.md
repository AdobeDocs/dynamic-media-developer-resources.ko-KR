---
description: 기본 보기는 정적 이미지, 정적 이미지 맨 위의 플라이아웃 보기에 표시된 확대 이미지, 정적 이미지 맨 위에 표시된 팁 메시지로 구성됩니다.
solution: Experience Manager
title: 플라이아웃 확대/축소 보기
feature: Dynamic Media Classic,Viewers,SDK/API,인라인 확대/축소
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# 플라이아웃 확대/축소 보기{#flyout-zoom-view}

기본 보기는 정적 이미지, 정적 이미지 맨 위의 플라이아웃 보기에 표시된 확대 이미지, 정적 이미지 맨 위에 표시된 팁 메시지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 보기의 CSS 속성**

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
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 기본 보기를 투명하게 만들려면:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**팁 메시지의 CSS 속성**

팁 메시지의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

CSS를 통해 글꼴 스타일, 크기 모양 및 세로 오프셋을 구성할 수 있습니다. 그러나 가로 맞춤은 뷰어 논리에 의해 관리됩니다. `left` 또는 `right` 속성을 사용하여 CSS를 통해 재정의하는 것은 지원되지 않습니다.

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
   <td colname="col2"> <p>기본 뷰의 하단에서 오프셋합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트 주위에 패딩합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트의 배경색 채우기 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 반경  </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트의 배경 테두리 반경. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도  </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트의 배경 불투명도입니다. </p> <p>Internet Explorer 8의 경우 <span class="codeph"> filter:alpha(opacity-..) </span> 사용 </p> </td> 
  </tr> 
 </tbody> 
</table>

팁 메시지는 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소 현지화](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27)를 참조하십시오.

.

예 - 흰색 Arial 12px 글꼴로 반투명 팁 메시지를 설정하려면 기본 보기 아래쪽에서 50픽셀 오프셋하고 패딩과 반올림된 테두리를 설정합니다.

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
