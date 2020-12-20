---
description: 기본 보기는 정적 이미지, 플라이아웃 보기에 표시된 확대/축소 이미지, 정적 이미지 위에 표시된 강조 표시 탐색 영역 및 정적 이미지 위에 표시된 팁 메시지로 구성됩니다.
seo-description: 기본 보기는 정적 이미지, 플라이아웃 보기에 표시된 확대/축소 이미지, 정적 이미지 위에 표시된 강조 표시 탐색 영역 및 정적 이미지 위에 표시된 팁 메시지로 구성됩니다.
seo-title: 플라이아웃 확대/축소 보기
solution: Experience Manager
title: 플라이아웃 확대/축소 보기
topic: Dynamic media
uuid: 35c60228-3044-442b-a8e2-e13d0bd306a5
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 2%

---


# 플라이아웃 확대/축소 보기{#flyout-zoom-view}

기본 보기는 정적 이미지, 플라이아웃 보기에 표시된 확대/축소 이미지, 정적 이미지 위에 표시된 강조 표시 탐색 영역 및 정적 이미지 위에 표시된 팁 메시지로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

보고 있는 이미지의 크기가 플라이아웃 확대/축소 보기의 크기와 일치하지 않으면 플라이아웃 확대/축소 보기의 사각형 표시 영역 중앙에 이미지 내용이 배치됩니다.

**기본 보기의 CSS 속성**

기본 보기의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
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

**플라이아웃 보기의 CSS 속성**

플라이아웃 보기의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기의 왼쪽 위 모서리를 기준으로 하는 플라이아웃 보기의 수평 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기의 왼쪽 위 모서리를 기준으로 하는 플라이아웃 보기의 수직 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 플라이아웃 보기의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>플라이아웃 보기의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>플라이아웃 보기의 테두리입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 이전 예제에 표시된 512 x 288 기본 보기의 오른쪽에 100픽셀 오프셋이 표시되는 플라이아웃 보기를 600 x 400픽셀로 설정하려면:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**기본 보기에서 강조 표시의 CSS 속성**

기본 보기에서 강조 표시의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

CSS를 사용하여 배경, 테두리, 투명도 및 유사한 속성을 제어할 수 있습니다. 그러나 강조 표시 DOM 요소의 크기 및 위치는 뷰어 논리로 관리됩니다. CSS를 통해 덮어쓰는 것은 지원되지 않습니다.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 강조 표시 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도  </span> </p> </td> 
   <td colname="col2"> <p> 불투명도를 강조 표시합니다. </p> <p>Internet Explorer 8의 경우 <span class="codeph"> 필터:alpha(opacity-...);</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>테두리가 강조 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 40% 투명도와 1픽셀의 빨강 테두리로 녹색 강조 표시를 설정하려면:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**커서의 CSS 속성**

`highlightmode` 매개 변수가 `cursor`으로 설정된 경우 기본 보기의 강조 표시가 고정 크기 커서 아트웍으로 대체되며, 이 아트웍은 CSS 클래스 선택기로 제어됩니다.

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

CSS를 사용하여 배경 이미지 및 크기를 제어할 수 있습니다.

적용 가능한 CSS 속성은 다음과 같습니다.

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>커서 아트웍을 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>커서 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>커서 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>커서는 다른 장치에 대해 서로 다른 커서 아트웍과 크기를 적용하는 데 사용할 수 있는 `input` 속성 선택기를 지원합니다. 특히, `input="mouse"`은 데스크톱 시스템에 해당하고 `input="touch"`은 터치 장치에 해당합니다.

**오버레이의 CSS 속성**

`overlay` 매개 변수가 `1`으로 설정된 경우 강조 프레임 주변 영역 또는 커서 이미지는 CSS 클래스 선택기로 제어됩니다.

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>오버레이 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도  </span> </p> </td> 
   <td colname="col2"> <p>오버레이 불투명도. </p> </td> 
  </tr> 
 </tbody> 
</table>

**팁 메시지의 CSS 속성**

팁 메시지의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

CSS를 통해 글꼴 스타일, 크기 모양 및 수직 오프셋을 구성할 수 있습니다. 그러나 가로 정렬은 뷰어 논리로 관리됩니다. `left` 또는 `right` 속성을 사용하여 CSS를 통해 덮어쓰는 것은 지원되지 않습니다.

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
   <td colname="col2"> <p>기본 보기의 아래쪽에서 오프셋합니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트 주위에 패딩합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트의 배경 채우기 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트의 배경 테두리 반경. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도  </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트의 배경 불투명도입니다. </p> <p>Internet Explorer 8의 경우 <span class="codeph"> 필터:alpha(opacity-...) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

팁 메시지를 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27)의 현지화를 참조하십시오.

예 - 기본 보기 아래쪽에서 흰색 Arial 12px 글꼴, 패딩 및 둥근 테두리로 반투명 팁 메시지를 설정하려면 다음을 수행합니다.

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

