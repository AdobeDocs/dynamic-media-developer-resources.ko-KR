---
title: 인쇄
description: 인쇄 도구는 도구가 활성화될 때 표시되는 모달 대화 상자와 컨트롤 모음에 추가된 단추로 구성됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c5939cdc-fa4e-4f19-b2a9-21b389492c4f
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 2%

---

# 인쇄{#print}

인쇄 도구는 도구가 활성화될 때 표시되는 모달 대화 상자와 컨트롤 모음에 추가된 단추로 구성됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

인쇄 단추의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7print
```

**인쇄 단추의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 상단 </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대의 상단으로부터 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 여백 </span> </p> </td> 
   <td colname="col2"> <p> 왼쪽의 다음 단추까지의 거리 또는 이 단추가 행의 첫 번째 단추인 경우 컨트롤 막대의 왼쪽에 있는 거리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>단추의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p>참조 - <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기. 다른 스킨을 다른 단추 상태에 적용하는 데 사용할 수 있습니다.

단추 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 추가 정보.

예 - 28 x 28픽셀인 인쇄 단추를 설정하고 네 개의 서로 다른 단추 상태에 대해 다른 이미지를 표시합니다.

```
.s7ecatalogsearchviewer .s7print { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7print[state='up'] { 
background-image:url(images/v2/Print_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7print[state='over'] { 
background-image:url(images/v2/Print_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7print[state='down'] { 
background-image:url(images/v2/Print_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7print[state='disabled'] { 
background-image:url(images/v2/Print_dark_disabled.png); 
}
```

대화 상자가 활성 상태일 때 웹 페이지를 덮는 배경 오버레이는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
```

**후면 오버레이의 CSS 속성**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도 </span> </p> </td> 
   <td colname="col2"> <p> 배경 오버레이 불투명도. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>배경 오버레이 색상. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 70% 불투명도를 사용하여 회색 오버레이를 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

기본적으로 모달 대화 상자가 데스크탑 시스템의 화면 중앙에 표시됩니다. 대화 상자의 위치 지정 및 크기 조절은 구성 요소에서 관리합니다. 대화 상자는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**대화 상자의 CSS 속성**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 반경 </span> </p> </td> 
   <td colname="col2"> <p> 대화 상자 테두리 반경. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 대화 상자 배경색; </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 회색 배경을 갖도록 대화 상자를 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

대화 상자 헤더는 아이콘, 제목 텍스트 및 닫기 단추로 구성됩니다. 헤더 컨테이너는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
```

**대화 상자 헤더의 CSS 속성**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 헤더 컨텐츠에 대한 내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

아이콘 및 제목 텍스트는 다음과 같이 제어되는 추가 컨테이너에 래핑됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
```

**대화 상자의 CSS 속성**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 헤더 아이콘 및 제목에 대한 내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

헤더 아이콘은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
```

**대화 상자 헤더 아이콘의 CSS 속성**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 이미지. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p>참조 - <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

헤더 제목은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
```

**대화 상자 헤더 텍스트의 CSS 속성**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>글꼴 가중치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 패밀리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 텍스트 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

닫기 단추는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
```

**닫기 단추의 CSS 속성 **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p> 헤더 컨테이너에 대한 세로 단추 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 헤더 컨테이너에 대한 가로 단추 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>단추 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>단추의 내부 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>각 상태에 대한 단추 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p>참조 - <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기. 다른 스킨을 다른 단추 상태에 적용하는 데 사용할 수 있습니다.

닫기 단추 도구 팁과 대화 상자 제목을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 추가 정보.

예 - 패딩, 22 x 22픽셀 아이콘 및 굵은 16포인트 제목을 사용하여 대화 상자 헤더를 설정하려면 다음을 수행하십시오. 마지막으로, 28x28픽셀 닫기 단추가 위쪽에서 2개의 픽셀과 대화 상자 컨테이너 오른쪽에서 2개의 픽셀을 배치했습니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgprint_cap.png"); 
    height: 22px; 
    width: 22px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

대화 상자 바닥글은 취소 및 인쇄로 보내기 단추로 구성됩니다. 바닥글 컨테이너는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
```

**대화 상자 바닥글의 CSS 속성 **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p> 대화 상자의 나머지 부분과 바닥글을 시각적으로 구분하는 데 사용할 수 있는 테두리입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

바닥글에는 두 단추를 모두 유지하는 내부 컨테이너가 있습니다. 이 컨트롤은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
```

**대화 상자 단추 컨테이너의 CSS 속성**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 바닥글과 단추 사이의 내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

취소 단추는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
```

**대화 상자의 CSS 속성 취소 단추**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>단추 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 각 상태에 대한 단추 텍스트 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 각 상태에 대한 단추 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기. 다른 스킨을 다른 단추 상태에 적용하는 데 사용할 수 있습니다.

인쇄로 보내기 단추는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**대화 상자 작업 단추의 CSS 속성**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>단추 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색상 </span> </p> </td> 
   <td colname="col2"> <p> 각 상태에 대한 단추 텍스트 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 각 상태에 대한 단추 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기. 다른 스킨을 다른 단추 상태에 적용하는 데 사용할 수 있습니다.

또한 두 단추 모두 다른 대화 상자 단추와 동일한 CSS 설정을 포함할 수 있는 일반적인 CSS 클래스를 공유합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
```

**단추의 CSS 속성**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 가중치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 모음입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 라인 높이 </span> </p> </td> 
   <td colname="col2"> <p> 단추 내부의 텍스트 높이. 세로 정렬에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상자 그림자 </span> </p> </td> 
   <td colname="col2"> <p>그림자. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 순익 </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 단추 여백. </p> </td> 
  </tr> 
 </tbody> 
</table>

단추 도구 설명은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 추가 정보.

예 - 64 x 34 취소 단추와 96 x 34 인쇄로 보내기 단추가 있는 대화 상자 바닥글을 설정하려면 각 단추 상태에 대해 텍스트 색상 및 배경색을 다르게 지정합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton { 
 width:96px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

머리글과 바닥글 사이에 있는 기본 대화 상자 영역에는 대화 상자 컨텐츠가 있습니다. 모든 경우 구성 요소는 이 영역의 너비를 관리하므로 CSS로 설정할 수 없습니다. 기본 대화 상자 영역은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**대화 상자의 CSS 속성 보기 영역 **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p> 주 대화상자 영역의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>기본 대화 상자 영역의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>외부 여백. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 자동으로 계산된 높이를 갖도록 기본 대화 상자 영역을 설정하려면 10개의 픽셀 여백을 사용하고 흰색 배경을 사용합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

모든 양식 컨텐츠(예: 레이블 및 입력 필드)는 다음 CSS 클래스 선택기를 사용하여 제어되는 컨테이너 내에 있습니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
```

**대화 상자 본문의 CSS 속성**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 양식 컨텐츠에 10픽셀 패딩을 포함하도록 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

대화 상자 양식은 라인별로 채워져 있으며 각 줄에는 양식 컨텐츠의 일부(레이블 및 텍스트 입력 필드 등)가 포함되어 있습니다. 단일 양식 선은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**대화 상자 줄의 CSS 속성**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 라인 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 각 행에 10픽셀 패딩이 있도록 대화 상자 양식을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

대화 상자 콘텐츠의 블록 크기는 다음 CSS 클래스 선택기로 제어됩니다.

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**대화 상자 입력 너비의 CSS 속성**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>블록 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 라인 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 컨텐츠 블록을 너비가 430픽셀이고 하단에서 패딩이 10픽셀로 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

대화 상자 양식의 모든 정적 레이블은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
```

이 클래스는 양식 사용자 인터페이스의 여러 위치에서 텍스트에 적용할 수 있으므로 레이블 크기 또는 위치를 제어하는 데 적합하지 않습니다.

**대화 상자 레이블의 CSS 속성입니다. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>레이블 글꼴 가중치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>레이블 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 패밀리에 레이블을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색상 </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상을 레이블 지정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

대화 상자 레이블은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 추가 정보.

예 - 9픽셀 글꼴로 회색, 굵게 모든 레이블을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

입력 컨트롤은 컨테이너에 래핑되고 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**대화 상자 입력 컨테이너의 CSS 속성**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 대화 상자의 왼쪽 가장자리에서 30픽셀 패딩을 설정합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

라디오 단추 및 해당 캡션 텍스트는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**대화 상자 옵션의 CSS 속성**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 캡션이 있는 라디오 단추의 총 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색상 </span> </p> </td> 
   <td colname="col2"> <p>캡션 텍스트 색상. </p> </td> 
  </tr> 
 </tbody> 
</table>

라디오 단추와 해당 캡션 사이의 간격은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**대화 상자 옵션 입력의 CSS 속성**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 순익 </span> </p> </td> 
   <td colname="col2"> <p> 라디오 단추와 해당 캡션 사이의 간격. </p> </td> 
  </tr> 
 </tbody> 
</table>

인쇄 범위 선택을 위한 숫자 선택기는 다음 CSS 클래스 선택기로 제어됩니다

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**대화 상자의 CSS 속성 인쇄 범위**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 숫자 선택기의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 </span> </p> </td> 
   <td colname="col2"> <p> 숫자 선택기 주변 간격. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 모든 라디오 단추를 검정 텍스트, 10픽셀 간격 및 42픽셀 너비 숫자 선택기를 사용하여 150픽셀 너비로 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption { 
    color: #000000; 
    width: 150px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption input { 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange { 
    margin-left: 10px; 
    margin-right: 10px; 
    width: 42px; 
}
```

페이지 범위 선택과 인쇄 레이아웃 섹션 간의 가로 구분선은 다음 CSS 클래스 선택기로 제어됩니다.

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**수평 분할기의 CSS 속성**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p> 구분선 주위에 테두리가 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>구분선 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 </span> </p> </td> 
   <td colname="col2"> <p>외부 여백 </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 양면에 10픽셀 수직 패딩과 맨 위에 10픽셀 여백이 있는 430픽셀 너비 회색 구분선을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```
