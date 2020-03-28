---
description: 즐겨찾기 메뉴 드롭다운 목록이 컨트롤 막대에 나타납니다. 사용자가 단추를 클릭하거나 탭하면 확장되는 버튼과 패널로 구성됩니다. 패널에는 개별 즐겨찾기 도구가 포함되어 있습니다.
seo-description: 즐겨찾기 메뉴 드롭다운 목록이 컨트롤 막대에 나타납니다. 사용자가 단추를 클릭하거나 탭하면 확장되는 버튼과 패널로 구성됩니다. 패널에는 개별 즐겨찾기 도구가 포함되어 있습니다.
seo-title: 즐겨찾기 메뉴
solution: Experience Manager
title: 즐겨찾기 메뉴
topic: Dynamic media
uuid: 46de2a74-690e-4010-8a71-54206dd02fd0
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 즐겨찾기 메뉴{#favorites-menu}

즐겨찾기 메뉴 드롭다운 목록이 컨트롤 막대에 나타납니다. 사용자가 단추를 클릭하거나 탭하면 확장되는 버튼과 패널로 구성됩니다. 패널에는 개별 즐겨찾기 도구가 포함되어 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

뷰어 사용자 인터페이스에서 즐겨찾기 메뉴의 위치 및 크기는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7favoritesmenu
```

**즐겨찾기 메뉴 단추의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대의 위쪽에서 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> 왼쪽의 다음 단추까지의 거리 또는 행의 첫 번째 단추인 경우 컨트롤 막대의 왼쪽입니다. </p> </td> 
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

예 - 컨트롤 막대 위쪽에서 4픽셀, 가장 가까운 단추에서 왼쪽으로 10픽셀, 크기 28 x 28픽셀의 즐겨찾기 메뉴를 설정합니다.

```
.s7ecatalogsearchviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

즐겨찾기 메뉴 버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton
```

**즐겨찾기 단추의 CSS 속성**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 속성 선택기를 지원합니다. 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 [내용은 사용자 인터페이스 요소의](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 현지화를 참조하십시오.

예 - 네 가지 서로 다른 단추 상태에 대해 서로 다른 이미지를 표시하는 즐겨찾기 메뉴 단추를 설정합니다.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

개별 즐겨찾기 아이콘이 포함된 패널의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel
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

예 - 투명한 색상을 갖도록 패널을 설정합니다.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

