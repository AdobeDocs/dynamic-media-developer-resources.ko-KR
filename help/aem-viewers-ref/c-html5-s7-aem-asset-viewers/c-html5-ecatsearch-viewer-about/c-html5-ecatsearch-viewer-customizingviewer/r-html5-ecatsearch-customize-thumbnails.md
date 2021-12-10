---
title: 썸네일
description: 축소판은 축소판 이미지의 격자로 구성되며 오른쪽에는 세로 스크롤을 할 수 있는 선택적 스크롤 막대가 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 25032917-237c-4227-92bd-ce66a6d003a0
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 2%

---

# 썸네일{#thumbnails}

축소판은 축소판 이미지의 격자로 구성되며 오른쪽에는 세로 스크롤을 할 수 있는 선택적 스크롤 막대가 있습니다.

기본 컨트롤 모음에서 축소판 그림 단추를 클릭하면 축소판이 전환됩니다. 미리 보기가 활성화되면 뷰어 사용자 인터페이스 위에 오버레이된 모달 모드로 표시됩니다. 뷰어 로직에서는 축소판 컨테이너의 크기를 전체 뷰어 영역으로 자동으로 조정합니다.

축소판 컨테이너의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7thumbnailgridview`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p> 뷰어 상단에서 축소판 컨테이너의 세로 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 상단 </span> </p> </td> 
   <td colname="col2"> <p>위쪽 여백. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 여백 </span> </p> </td> 
   <td colname="col2"> <p>왼쪽 여백. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 순익 </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 여백. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 하단 </span> </p> </td> 
   <td colname="col2"> <p>아래 여백. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>축소판 영역의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 축소판을 설정하려면 위에서 32픽셀 오프셋, 왼쪽과 오른쪽에 5픽셀 여백, 아래에 8픽셀 여백이 있으며 `0xDDDDDD` 배경.

```
.s7ecatalogsearchviewer .s7thumbnailgridview { 
 top: 32px; 
 margin-left: 5px; 
 margin-right: 5px; 
 margin-bottom: 8px; 
 background-color: rgb(221, 221, 221); 
}
```

축소판 간의 간격은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumbcell`

<table id="table_1D93AB60E57F49A8838EA825CD6B7897"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 각 축소판 주위의 가로 및 세로 여백의 크기입니다. 실제 가로 축소판 간격은 <span class="codeph"> .s7thumbcell </span>. 세로 축소판 간격은 위쪽 및 아래쪽 여백의 합과 같습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 세로 및 가로로 모두 10픽셀 공간을 설정합니다.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumbcell { 
 margin: 5px; 
}
```

개별 축소판의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb`

<table id="table_1D973EA6C36947F092AAA16CFE9B44A1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>축소판의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>축소판의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>축소판의 테두리입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>축소판의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

터치 장치에서 세로 모드로 회전할 때 뷰어는 카탈로그 스프레드를 개별 페이지로 분할하기로 결정하는 경우 구성된 사항의 절반까지 축소판의 크기를 조정할 수 있습니다.

>[!NOTE]
>
>축소판 그림 은 `state` 속성 선택기. 다른 스킨을 다른 축소판 상태에 적용하는 데 사용할 수 있습니다. 특히, `state="selected"` 는 현재 기본 보기에 표시되는 이미지의 축소판에 해당합니다. `state="default"` 는 나머지 축소판에 해당하며 `state="over"` 마우스로 가리키면 사용됩니다.

예 - 120 x 85픽셀로 축소판을 설정하려면 흰색 배경, 밝은 회색 표준 테두리 및 어두운 회색으로 선택한 테두리를 사용합니다.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb { 
 width:120px; 
 height:85px; 
 background-color: rgb(255, 255, 255); 
 border: solid 1px #999999; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb[state="selected"]{ 
 border: solid 2px #666666; 
}
```

축소판 레이블의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7label`

<table id="table_E242176042F247F8B51A0D5ADB645E20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 14픽셀 Helvetica® 글꼴을 사용하도록 레이블을 설정합니다.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 12px; 
}
```

보기에 세로로 맞출 수 있는 것보다 더 많은 축소판이 있는 경우 축소판이 오른쪽의 세로 스크롤 막대를 렌더링합니다. 스크롤 막대 영역의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar`

<table id="table_F05EC87CD9A946DB9B4B2B48E0784168"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 막대의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p> 축소판 영역의 맨 위에서 수직 스크롤 막대 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>축소판 영역의 아래쪽에서 수직 스크롤 막대 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 축소판 영역의 오른쪽 모서리에서 벗어난 가로 스크롤 막대 오프셋입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 28픽셀 너비로 축소판 영역의 위쪽, 오른쪽 및 아래쪽에서 8픽셀 여백이 있는 스크롤 막대를 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar { 
 top:8px; 
 bottom:8px; 
 right:8px; 
 width:28px; 
}
```

스크롤 막대 트랙은 위쪽 및 아래쪽 스크롤 단추 사이의 영역입니다. 구성 요소는 트랙의 위치와 높이를 자동으로 설정합니다. 트랙은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack`

<table id="table_EF1B91F9E984451EB0AB48175D917726"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 막대 트랙의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 막대 트랙의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 가로 28픽셀이고 반투명 회색 배경을 포함하는 스크롤 막대 트랙을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

스크롤 막대 엄지는 스크롤 트랙 영역 내에서 세로로 이동합니다. 세로 위치는 구성 요소 로직에 의해 완전히 제어되지만 엄지 높이는 컨텐츠 양에 따라 동적으로 변경되지 않습니다. 엄지 높이 및 기타 측면이 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb`

<table id="table_5C791F6E90E64E7A9F1DB7C9B2FDC528"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 막대 엄지손가락의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 막대 축소판의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 탑 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 막대 트랙의 상단 사이의 수직 안쪽 여백입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 하단 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 막대 트랙 아래쪽의 수직 안쪽 여백입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>주어진 경험 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p>참조 - <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb은 `state` 특성 선택기. thumb 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다 `up`, `down`, `over`, 및 `disabled`.

예 - 28 x 45픽셀인 스크롤 막대 엄지를 설정하려면 위쪽과 아래쪽에 10픽셀 여백이 있고 각 상태에 대해 서로 다른 아트웍을 사용합니다.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

위쪽 및 아래쪽 스크롤 단추의 모양은 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton`

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton`

CSS를 사용하여 스크롤 단추를 배치할 수 없습니다 `top`, `left`, `bottom`, 및 `right` 속성을 사용합니다. 대신 뷰어 논리에서 자동으로 위치를 지정합니다.

<table id="table_89E64A138ABF463F9650BB454F22D530"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>단추의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>주어진 경험 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p>참조 - <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이러한 버튼은 `state` 속성 선택기: 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다 `up`, `down`, `over`, 및 `disabled`.

단추 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 추가 정보.

예 - 28 x 32픽셀이며 각 상태에 대해 서로 다른 아트웍을 갖는 스크롤 단추를 설정합니다.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
