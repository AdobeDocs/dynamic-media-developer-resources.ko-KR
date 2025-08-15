---
title: 즐겨찾기 효과
description: 뷰어는 사용자가 처음 추가한 위치의 기본 보기 위에 즐겨찾기 아이콘을 표시합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# 즐겨찾기 효과{#favorites-effect}

뷰어는 사용자가 처음 추가한 위치의 기본 보기 위에 즐겨찾기 아이콘을 표시합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

즐겨찾기 아이콘의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

즐겨찾는 아이콘의 **CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 아이콘에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 높이. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 36x36픽셀 즐겨찾기 아이콘을 설정합니다.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

데스크톱 시스템에서 구성 요소는 `cursortype` 클래스에 적용할 수 있는 `.s7favoriteseffect` 특성 선택기를 지원하고 선택한 사용자 작업을 기반으로 커서 형식을 제어합니다. 다음 `cursortype` 값이 지원됩니다.

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
   <td colname="col2"> <p>즐겨찾기 편집이 활성화되지 않은 경우 일반 작업 모드로 표시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 구성 요소 상태 유형마다 다른 마우스 커서를 보유합니다.

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
