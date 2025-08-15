---
title: 목차
description: 목차는 기본 컨트롤 막대에 있는 단추입니다. 활성화되면 페이지 인덱스 및 레이블 목록이 포함된 드롭다운 패널이 표시됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: bc597c68-b86c-4577-9d24-6999eccada78
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# 목차{#table-of-contents}

목차는 기본 컨트롤 막대에 있는 단추입니다. 활성화되면 페이지 인덱스 및 레이블 목록이 포함된 드롭다운 패널이 표시됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

구성에 따라 목록에는 카탈로그에 있는 모든 페이지나 명시적 레이블이 정의된 페이지만 포함될 수 있습니다. 데스크탑 시스템에서는 목록이 사용 가능한 화면 부동산보다 긴 경우 오른쪽에 스크롤 막대가 표시됩니다.

뷰어 사용자 인터페이스에서 목차 버튼의 위치와 크기는 다음 CSS 클래스 선택기로 제어합니다.

```
.s7ecatalogsearchviewer .s7tableofcontents
```

**목차의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-상단 </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대의 위쪽에 있는 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-왼쪽 </span> </p> </td> 
   <td colname="col2"> <p> 왼쪽에 있는 다음 단추까지의 거리 또는 이 단추가 행의 첫 번째 단추인 경우 컨트롤 막대의 왼쪽입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 목차 버튼의 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p> 목차 버튼의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 특성 선택기를 지원하며, 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

예 - 기본 컨트롤 막대의 맨 아래에서 4픽셀, 왼쪽에서 43픽셀로 배치된 목차 단추를 설정합니다. 크기는 28 x 28픽셀이며 4개의 서로 다른 버튼 상태 각각에 대해 다른 이미지가 표시됩니다.

```
.s7ecatalogsearchviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

드롭다운 패널의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel
```

**드롭다운 패널의 CSS 속성**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 드롭다운 패널의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 </span> </p> </td> 
   <td colname="col2"> <p> 패널 경계와 컨텐츠 간의 내부 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상자-그림자 </span> </p> </td> 
   <td colname="col2"> <p> 패널 주위에 그림자를 그립니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>CSS에서 드롭다운 패널의 크기나 위치를 제어할 수 없습니다. 구성 요소는 레이아웃을 프로그래밍 방식으로 관리합니다.

예 - 반투명 검은색 배경, 콘텐츠 주위의 5픽셀 여백 및 그림자 효과가 있는 드롭다운 패널을 설정합니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

개별 항목 모양과 느낌은 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item
```

**항목의 CSS 속성**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>항목의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>드롭다운 목록 항목은 `state` 특성 선택기를 지원하며, 이 선택기는 마우스로 가리키거나 선택한 항목 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

예 - Helvetica® 14픽셀 글꼴과 19픽셀 높이의 드롭다운 항목을 설정합니다. 항목을 선택하면 마우스로 가리키고 밝은 회색 배경이 있는 어두운 회색 배경이 있습니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

페이지 인덱스를 표시하는 요소는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index
```

**페이지 인덱스의 CSS 속성**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">분 너비 </span> </p> </td> 
   <td colname="col2"> <p> 최소 요소 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최대 너비 </span> </p> </td> 
   <td colname="col2"> <p> 최대 요소 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 페이지 색인과 페이지 레이블 간의 거리입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>`display:none` CSS 클래스에 대해 `s7index`을(를) 설정하여 페이지 인덱스를 완전히 숨길 수 있습니다.

예제 1 - 오른쪽에서 최소 너비가 40픽셀이고 최대 너비가 70픽셀이며 5픽셀 여백이 있는 페이지 인덱스를 설정합니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

예제 2 - 페이지 인덱스 숨기기:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

페이지 레이블은 다음 CSS 클래스 선택기로 제어됩니다.

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label
```

**페이지 레이블의 CSS 속성**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">분 너비 </span> </p> </td> 
   <td colname="col2"> <p> 최소 요소 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최대 너비 </span> </p> </td> 
   <td colname="col2"> <p> 최대 요소 너비입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 최소 너비는 40픽셀이고 최대 너비는 240픽셀인 페이지 인덱스를 설정합니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

드롭다운 패널 내에 세로로 맞출 수 있는 것보다 많은 항목이 있고 시스템이 데스크탑인 경우 구성 요소는 패널의 오른쪽에 있는 세로 스크롤 막대를 렌더링합니다. 스크롤 막대 영역의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar
```

**스크롤 막대의 CSS 속성**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 막대 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p> 패널 영역의 위쪽에서 오프셋된 세로 스크롤 막대입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 패널 영역 아래쪽에서 오프셋된 세로 스크롤 막대입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 패널 영역의 오른쪽 가장자리에서 오프셋된 가로 스크롤 막대입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 패널의 위쪽, 오른쪽 또는 아래쪽 영역에 여백이 없는 28픽셀 너비의 스크롤 막대를 설정합니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

스크롤 막대 트랙은 위쪽 및 아래쪽 스크롤 단추 사이의 영역입니다. 이 구성 요소는 트랙의 위치와 높이를 자동으로 설정합니다. 트랙은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**스크롤 트랙의 CSS 속성**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>트랙 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>트랙 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 폭이 28픽셀이고 배경이 반투명한 스크롤바 트랙을 설정합니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

스크롤 막대 썸네일이 스크롤 트랙 영역 내에서 세로로 이동합니다. 수직 위치는 구성 요소 논리에 의해 제어됩니다. 그러나 썸네일 높이는 컨텐츠의 양에 따라 동적으로 변경되지 않습니다. 다음 CSS 클래스 선택기를 사용하여 썸네일 높이 및 기타 측면을 구성할 수 있습니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**스크롤 막대 썸네일의 CSS 속성**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>썸네일 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>엄지 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 상단 </span> </p> </td> 
   <td colname="col2"> <p> 트랙 상단 사이의 수직 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩-하단 </span> </p> </td> 
   <td colname="col2"> <p>트랙 하단 사이의 수직 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 지정된 썸네일 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb은 `state`, `up`, `down` 및 `over` Thumb 상태에 다른 스킨을 적용하는 데 사용할 수 있는 `disabled` 특성 선택기를 지원합니다.

예 - 28 x 45픽셀이고 위쪽과 아래쪽에 10픽셀 여백이 있으며 각 상태에 대해 서로 다른 아트워크가 있는 스크롤 막대 썸을 설정합니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

다음 CSS 클래스 선택기를 사용하여 위쪽 및 아래쪽 스크롤 단추의 모양이 제어됩니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

CSS `top`, `left`, `bottom` 및 `right` 속성을 사용하여 스크롤 단추를 배치할 수 없습니다. 대신 뷰어 논리에서 자동으로 배치합니다.

**위로 스크롤 및 아래로 스크롤 단추의 CSS 속성**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>단추 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>단추는 `state`, `up`, `down` 및 `over` 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있는 `disabled` 특성 선택기를 지원합니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

예 - 28 x 32픽셀이며 각 상태에 대해 다른 아트웍이 있는 스크롤 단추를 설정합니다.

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
