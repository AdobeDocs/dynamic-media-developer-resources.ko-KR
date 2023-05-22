---
title: 즐겨찾기 메뉴
description: 즐겨찾기 메뉴 드롭다운 목록이 컨트롤 막대에 나타납니다. 사용자가 버튼을 클릭하거나 탭하면 확장되는 버튼과 패널로 구성된다. 패널에는 개별 즐겨찾기 도구가 포함되어 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3c90320-b6fc-4a43-b75f-d39234b1e73c
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# 즐겨찾기 메뉴{#favorites-menu}

즐겨찾기 메뉴 드롭다운 목록이 컨트롤 막대에 나타납니다. 사용자가 버튼을 클릭하거나 탭하면 확장되는 버튼과 패널로 구성된다. 패널에는 개별 즐겨찾기 도구가 포함되어 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

뷰어 사용자 인터페이스에서 즐겨찾기 메뉴의 위치 및 크기는 다음 CSS 클래스 선택기로 제어합니다.

```
.s7ecatalogviewer .s7favoritesmenu
```

**즐겨찾기 메뉴 버튼의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-상단 </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대의 위쪽에 있는 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 여백 </span> </p> </td> 
   <td colname="col2"> <p> 왼쪽에 있는 다음 단추까지의 거리 또는 한 행에 있는 첫 번째 단추인 경우 컨트롤 막대의 왼쪽입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>단추의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 컨트롤 막대의 맨 위에서 4픽셀, 왼쪽에서 가장 가까운 단추에서 10픽셀, 크기가 28 x 28픽셀인 즐겨찾기 메뉴를 설정하려면 다음을 수행합니다.

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

즐겨찾기 메뉴 버튼의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**즐겨찾기 버튼의 CSS 속성**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>참조: <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기: 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 추가 정보.

예 - 네 가지 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시하는 즐겨찾기 메뉴 단추를 설정하려면 다음을 수행합니다.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

개별 즐겨찾기 아이콘이 포함된 패널의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**즐겨찾기 메뉴 패널의 CSS 속성**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>패널의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 패널을 투명한 색상으로 설정하려면 다음을 수행합니다.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```
