---
description: 단추의 위치는 즐겨찾기 메뉴에서 완전히 관리됩니다.
seo-description: 단추의 위치는 즐겨찾기 메뉴에서 완전히 관리됩니다.
seo-title: 모든 즐겨찾기 보기 단추
solution: Experience Manager
title: 모든 즐겨찾기 보기 단추
topic: Dynamic media
uuid: f9fd2110-d225-4eba-8e21-acc9c0e1dfd4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# 모든 즐겨찾기 보기 단추{#view-all-favorites-button}

단추의 위치는 즐겨찾기 메뉴에서 완전히 관리됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

[모든 즐겨찾기 보기] 단추의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7viewallfavoritebutton
```

**즐겨찾기 제거 단추의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
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

>[!NOTE]
>
>이 단추는 `state` 및 `selected` 속성 선택기를 모두 지원합니다. 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히, `selected='true'`은 사용자가 클릭하거나 탭하여 새 즐겨찾기 아이콘을 추가할 수 있는 상태에 해당합니다. `selected='false'` 사용자가 페이지를 확대/축소, 이동 및 교체할 수 있는 일반적인 작업 모드에 해당합니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 28 x 28픽셀인 [모든 즐겨찾기 보기] 단추를 설정하고 선택 또는 선택하지 않을 때 4개의 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시하려면

```
.s7ecatalogviewer .s7viewallfavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_up.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_down.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_disabled.png); 
}
```

