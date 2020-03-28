---
description: 뷰어는 사용자가 원래 추가한 위치에서 기본 보기 위에 즐겨찾기 아이콘을 표시합니다.
seo-description: 뷰어는 사용자가 원래 추가한 위치에서 기본 보기 위에 즐겨찾기 아이콘을 표시합니다.
seo-title: 즐겨찾기 효과
solution: Experience Manager
title: 즐겨찾기 효과
topic: Dynamic media
uuid: b660b9fd-592b-4072-83c9-f70330ee19ab
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 즐겨찾기 효과{#favorites-effect}

뷰어는 사용자가 원래 추가한 위치에서 기본 보기 위에 즐겨찾기 아이콘을 표시합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

즐겨찾기 아이콘의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**즐겨찾기 아이콘의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 아이콘에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>아이콘의 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>아이콘의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 36 x 36 픽셀 즐겨찾기 아이콘을 설정합니다.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

데스크톱 시스템에서 구성 요소는 `cursortype` 속성 선택기를 지원하며 `.s7favoriteseffect` 클래스에 적용할 수 있으며 선택한 사용자 작업에 따라 커서 유형을 제어합니다. The following `cursortype` values are supported:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>표시된 사용자가 새 즐겨찾기 아이콘을 추가하고 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>표시된 사용자가 기존 즐겨찾기 아이콘을 제거하고 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>즐겨찾기 편집이 활성 상태가 아닐 때 일반 작업 모드로 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 각 구성 요소 상태 유형에 대해 서로 다른 마우스 커서를 가지고 있습니다.

```
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```

