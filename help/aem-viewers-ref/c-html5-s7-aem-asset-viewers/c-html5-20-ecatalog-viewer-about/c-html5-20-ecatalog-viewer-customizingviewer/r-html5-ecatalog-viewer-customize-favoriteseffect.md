---
title: 즐겨찾기 효과
description: 뷰어는 사용자가 원래 추가한 위치에서 기본 보기 위에 즐겨찾기 아이콘을 표시합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---

# 즐겨찾기 효과{#favorites-effect}

뷰어는 사용자가 원래 추가한 위치에서 기본 보기 위에 즐겨찾기 아이콘을 표시합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

즐겨찾기 아이콘 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**즐겨찾기 아이콘 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 아이콘에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p>참조 - <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>아이콘의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>아이콘 높이입니다. </p> </td> 
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

데스크탑 시스템에서 구성 요소는 `cursortype` 에 적용할 수 있는 속성 선택기 `.s7favoriteseffect` 클래스 및 는 선택한 사용자 작업을 기반으로 커서 유형을 제어합니다. 다음 `cursortype` 지원되는 값은 다음과 같습니다.

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

예 - 각 구성 요소 상태 유형에 대해 서로 다른 마우스 커서를 가지려면

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
