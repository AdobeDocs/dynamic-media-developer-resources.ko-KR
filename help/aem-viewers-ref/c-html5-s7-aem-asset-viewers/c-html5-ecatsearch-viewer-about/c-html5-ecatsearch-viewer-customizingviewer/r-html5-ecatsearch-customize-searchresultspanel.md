---
title: 검색 결과 패널
description: 검색 결과 패널은 맨 위에 있는 검색 입력 상자와 정보 메시지 또는 검색 결과가 표시되는 기본 영역으로 구성됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 1%

---

# 검색 결과 패널{#search-results-panel}

검색 결과 패널은 맨 위에 있는 검색 입력 상자와 정보 메시지 또는 검색 결과가 표시되는 기본 영역으로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

패널이 활성화되면 뷰어 사용자 인터페이스는 반투명 채우기로 덮여 있습니다. 이 채우기의 색상 및 불투명도는 다음 CSS 클래스 선택기로 제어합니다.

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>오버레이의 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도 </span> </p> </td> 
   <td colname="col2"> <p>색상의 불투명도입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

검색 결과 패널은 항상 사용 가능한 모든 뷰어 높이를 차지합니다. 그러나 너비는 구성할 수 있습니다. 너비를 절대 픽셀 값으로 설정할 수 있습니다. 이 값은 중간 및 큰 크기의 중단점에 대한 기본 설정입니다. 또는 너비를 100%로 설정하여 검색 결과 패널이 전체 뷰어 영역을 차지하도록 할 수 있습니다. 패널 너비는 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**검색 결과 공간의 CSS 속성**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 검색 결과 공간 폭입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 큰 중단점과 중간 중단점에 250픽셀 너비의 검색 결과 패널을 설정하고 작은 중단점에 전체 크기 패널을 사용하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

검색 결과 패널 상단은 검색 입력 상자 전용입니다. 입력 상자의 측면에 있는 패딩은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**검색 입력 컨테이너의 CSS 속성**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 입력 상자 주변의 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

검색 입력 필드는 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**검색 입력 필드의 CSS 속성**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>검색 입력 필드의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩-왼쪽 </span> </p> </td> 
   <td colname="col2"> <p> 입력 필드 경계와 입력 텍스트 사이의 내부 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>검색 입력 필드의 테두리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>검색 입력 필드의 여백 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>텍스트 글꼴 크기입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 0픽셀 높이 및 14픽셀 텍스트 글꼴로 검색 입력 필드를 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

기본적으로 &quot;보이는 유리&quot; 형태의 검색 입력 필드 왼쪽에 있는 검색 단추는 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**검색 입력 버튼의 CSS 속성**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>검색 입력 단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>검색 입력 단추의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>"보이는 유리" 아이콘 이미지의 URL입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-size </span> </p> </td> 
   <td colname="col2"> <p>"보이는 유리" 아이콘 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>검색 입력 단추의 테두리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>검색 입력 단추의 여백입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 26 x 26픽셀 &quot;보이는 유리&quot; 아이콘으로 검색 단추를 설정하려면(1픽셀 테두리로 30픽셀):

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

검색 결과 패널은 특징이 처음 호출될 때 텍스트 프롬프트를 표시할 수 있다. 또한 사용자의 검색 결과가 반환되지 않은 경우에도 메시지가 표시됩니다. 모든 경우 텍스트는 검색 결과 패널의 주 부분에 표시되며 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**검색 정보의 CSS 속성**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>텍스트 글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>가로 텍스트 정렬. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 텍스트 크기입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 텍스트 패널은 `state` 속성 선택기: 다른 텍스트 메시지에 다른 스타일을 적용하는 데 사용할 수 있습니다. 특히, `state='prompt'` 패널이 처음 호출될 때 표시되는 텍스트 프롬프트에 해당합니다. 다음 `state='results'` 은 검색 히트에 대한 정보가 있는 텍스트에 해당합니다. 그리고 마지막으로 `state='no_results'` 검색 쿼리가 결과를 반환하지 않았을 때 표시되는 텍스트에 해당합니다.

메시지 텍스트를 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 추가 정보.

예 - 회색 18픽셀 글꼴을 사용하는 텍스트 패널을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

검색 결과는 검색 히트가 있는 페이지에 대해 단일 열 또는 단일 썸네일 행으로 렌더링됩니다. 검색 결과 썸네일 간의 간격은 다음 CSS 클래스 선택기로 제어됩니다.

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**썸네일 셀의 CSS 속성**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 각 썸네일 주변의 세로 여백 크기입니다. 실제 썸네일 간격은 다음에 대해 설정된 위쪽 및 아래쪽 여백의 합계와 같습니다. <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 10개의 픽셀 간격을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

개별 썸네일의 모양은 다음 CSS 클래스 선택기를 사용하여 제어합니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**썸네일의 CSS 속성**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 테두리. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 215 x 129픽셀인 썸네일을 설정하려면 밝은 회색의 기본 테두리와 어두운 회색의 선택된 테두리를 사용합니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

썸네일 레이블의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**레이블의 CSS 속성**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>텍스트 글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>텍스트 글꼴 크기입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 12픽셀, 회색, Helvetica® 글꼴을 사용하는 레이블을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

마우스 입력을 사용하는 시스템에서는 검색 결과 패널 하단에 두 개의 스크롤 단추가 표시되어 사용자가 검색 결과를 스크롤할 수 있습니다. 위 및 아래 스크롤 단추의 모양은 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

CSS 위쪽, 왼쪽, 아래쪽 및 오른쪽 속성을 사용하여 스크롤 단추를 배치할 수 없습니다. 대신 뷰어 로직은 뷰어를 자동으로 배치합니다.

**위로 및 아래로 스크롤 단추의 CSS 속성**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>스크롤 단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>스크롤 단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>참조: <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기: 다른 스킨을 적용하는 데 사용할 수 있습니다. `"up"`, `"down"`, `"over"`, 및 `"disabled"` 단추 상태.

버튼 도구 팁은 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 추가 정보.

예 - 125 x 35픽셀이며 각 상태에 대해 다른 아트웍이 있는 위로 스크롤 단추를 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```
