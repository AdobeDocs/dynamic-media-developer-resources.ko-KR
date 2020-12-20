---
description: 주 제어 막대는 eCatalog 검색 뷰어에 사용할 수 있는 모든 사용자 인터페이스 컨트롤(큰 페이지 단추 제외)이 포함된 데스크톱 시스템 및 태블릿의 사각형 영역입니다.
seo-description: 주 제어 막대는 eCatalog 검색 뷰어에 사용할 수 있는 모든 사용자 인터페이스 컨트롤(큰 페이지 단추 제외)이 포함된 데스크톱 시스템 및 태블릿의 사각형 영역입니다.
seo-title: 기본 컨트롤 막대
solution: Experience Manager
title: 기본 컨트롤 막대
topic: Dynamic media
uuid: 21b6e6cd-115f-4c7b-a61e-34b307142045
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 1%

---


# 기본 컨트롤 막대{#main-control-bar}

주 제어 막대는 eCatalog 검색 뷰어에 사용할 수 있는 모든 사용자 인터페이스 컨트롤(큰 페이지 단추 제외)이 포함된 데스크톱 시스템 및 태블릿의 사각형 영역입니다.

휴대폰에서는 축소판, 목차, 다운로드, 인쇄, 즐겨찾기, 소셜 공유, 전체 화면 및 닫기 단추가 그대로 유지됩니다. 그러나 [첫 페이지] 및 [마지막 페이지] 단추 및 [페이지 표시기]는 기본 컨트롤 모음에서 제거되고 대신 보조 컨트롤 막대에 추가됩니다. 기본적으로 기본 컨트롤 막대는 데스크톱 시스템 및 휴대 전화의 뷰어 영역 맨 위에 표시되고 태블릿의 뷰어 영역 맨 아래로 이동됩니다. 항상 사용 가능한 전체 뷰어 너비를 사용합니다. 뷰어 컨테이너를 기준으로 CSS의 색상, 높이 및 세로 위치를 변경할 수 있습니다.

기본 컨트롤 막대의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 상단에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 아래쪽의 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 높이가 36픽셀이고 뷰어 컨테이너의 상단에 위치한 회색 기본 컨트롤 막대를 설정하려면

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

기본 제어 막대는 선택적인 스크롤 기능을 지원합니다. 뷰어 너비가 너무 작고 컨트롤 막대에 미리 설정된 모든 단추에 맞출 공간이 충분하지 않으면 활성화됩니다. 이 경우 컨트롤 막대의 오른쪽에 두 상태 화살표 단추가 나타납니다. 이 단추를 클릭하거나 탭하면 스크롤 단추 상태에 따라 모든 컨트롤 막대 요소가 왼쪽 또는 오른쪽으로 스크롤됩니다. 이 기능의 기본 사용 사례는 세로 방향의 작은 화면이 있는 모바일 장치입니다.

스크롤 기능은 기본 제어 막대에 대해 활성화되며 보조 제어 막대에 대해 비활성화됩니다. 이 기능은 다음과 같은 CSS 클래스 선택기를 사용하여 켜거나 꺼집니다.

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 위치 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 정적 </span>으로 설정하면 스크롤 기능이 비활성화됩니다. </p> <p>스크롤 기능을 사용하려면 이 속성을 <span class="codeph"> 절대 </span>로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

스크롤 단추는 단추를 제대로 배치하는 특수 컨테이너 요소에 추가되며 스크롤 단추의 높이가 제어 막대 높이보다 작은 경우에 대비해 나머지 컨트롤 막대 배경과는 다르게 단추 주위의 영역에 스타일을 지정할 수 있습니다.

이 스크롤 단추 컨테이너의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>일반적으로 스크롤 단추 자체의 폭과 같거나 커야 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>컨테이너 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS를 통해 스크롤 단추 자체의 크기를 조정하고 스킨을 지정할 수 있습니다.

이 버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>단추 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p>CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 및 `selected` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히, `state="selected"`은 컨트롤 막대 내용을 왼쪽으로 스크롤할 수 있을 때 초기 스크롤 단추 상태에 해당합니다.`state="default"`은 컨텐츠가 왼쪽으로 완전히 스크롤될 때 초기 상태로 되돌리도록 스크롤 단추에서 제안하는 상태에 해당합니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

**예**  - 휴대 전화의 주 제어 막대에서 스크롤 기능을 활성화하고, 선택 여부와 관계없이 4개의 서로 다른 단추 상태에 대해 다른 이미지를 표시하는 64 x 64픽셀의 스크롤 단추를 설정하려면:

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```

