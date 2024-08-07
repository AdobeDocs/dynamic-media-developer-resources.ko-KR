---
title: 공유 포함
description: 공유 포함 도구는 소셜 공유 패널에 추가된 버튼과 도구가 활성화될 때 표시되는 모달 대화 상자로 구성됩니다. 버튼의 위치는 소셜 공유 도구에서 완전히 관리됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e29a81b8-67f3-4367-b21c-d5902420bc85
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '2617'
ht-degree: 0%

---

# 공유 포함{#embed-share}

공유 포함 도구는 소셜 공유 패널에 추가된 버튼과 도구가 활성화될 때 표시되는 모달 대화 상자로 구성됩니다. 버튼의 위치는 소셜 공유 도구에서 완전히 관리됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

다음 CSS 클래스 선택기를 사용하여 공유 포함 단추의 모양이 제어됩니다.

```
.s7videoviewer .s7embedshare
```

**포함 공유 도구의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
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
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 특성 선택기를 지원하며, 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

CSS 클래스에서 `display:none` CSS 속성을 설정하여 소셜 공유 패널에서 단추를 제거할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)를 참조하십시오.

예 - 28 x 28픽셀이고 네 개의 서로 다른 버튼 상태에 대해 각각 다른 이미지를 표시하는 포함 공유 단추를 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7videoviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7videoviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7videoviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

대화 상자가 활성 상태일 때 웹 페이지를 덮는 배경 오버레이는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7backoverlay
```

**백그라운드 오버레이의 CSS 속성**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도 </span> </p> </td> 
   <td colname="col2"> <p>배경 오버레이 불투명도. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>배경 오버레이 색상. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 배경 오버레이를 불투명도가 70%인 회색으로 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

기본적으로 모달 대화 상자는 데스크탑 시스템에서 화면 중앙에 표시되며 터치 디바이스에서 전체 웹 페이지 영역을 가져옵니다. 모든 경우 대화 상자의 위치 지정 및 크기 조정은 구성 요소에 의해 관리됩니다. 이 대화 상자는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialog
```

대화 상자의 **CSS 속성**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 대화 상자가 전체 브라우저를 사용하지 않는 경우 대화 상자 테두리 반경입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>대화 상자 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>를 설정 해제하거나 100%로 설정해야 합니다. 이 경우 대화 상자는 전체 브라우저 창을 사용합니다(이 모드는 터치 장치에서 선호됨). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>를 설정 해제하거나 100%로 설정해야 합니다. 이 경우 대화 상자는 전체 브라우저 창을 사용합니다(이 모드는 터치 장치에서 선호됨). </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 전체 브라우저 창을 사용하고 터치 장치에 흰색 배경을 포함하도록 대화 상자를 설정하려면:

```
.s7videoviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

대화 상자 머리글은 아이콘, 제목 텍스트 및 닫기 단추로 구성됩니다. 헤더 컨테이너는

```
.s7videoviewer .s7embeddialog .s7dialogheader
```

대화 상자 헤더의 **CSS 속성**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 헤더 콘텐츠에 대한 내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

아이콘과 제목 텍스트는 로 제어되는 추가 컨테이너에 래핑됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogheader .s7dialogline
```

대화 상자의 **CSS 속성**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 헤더 아이콘 및 제목의 내부 패딩 </p> </td> 
  </tr> 
 </tbody> 
</table>

헤더 아이콘은 다음 CSS 클래스 선택기로 제어됩니다

```
.s7videoviewer .s7embeddialog .s7dialogheadericon
```

대화 상자 헤더 아이콘의 **CSS 속성**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 이미지 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

헤더 제목은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogheadertext
```

대화 상자 헤더 텍스트의 **CSS 속성**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 모음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 텍스트 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

닫기 단추는 다음 CSS 클래스 선택기로 제어합니다.

```
.s7videoviewer .s7embeddialog .s7closebutton
```

**닫기 단추 속성의 CSS **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p> 머리글 컨테이너를 기준으로 한 세로 단추 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 헤더 컨테이너를 기준으로 한 가로 단추 위치. </p> </td> 
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
   <td colname="col2"> <p>단추의 내부 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>각 상태에 대한 단추 이미지. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 특성 선택기를 지원하며, 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

닫기 단추 도구 팁과 대화 상자 제목을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)를 참조하십시오.

예 - 패딩이 있는 대화 상자 헤더를 설정하려면 24 x 14픽셀 아이콘, 굵게 16포인트 제목을 설정합니다. 그리고 마지막으로 28 x 28픽셀 닫기 버튼이 있으며 대화 상자 컨테이너의 맨 위에서 2픽셀, 오른쪽에서 2픽셀을 배치했습니다.

```
.s7videoviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

대화 상자 바닥글은 &quot;취소&quot; 단추로 구성됩니다. 바닥글 컨테이너는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogfooter
```

**대화 상자 바닥글 속성의 CSS **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 </span> </p> </td> 
   <td colname="col2"> <p> 대화 상자의 나머지 부분과 바닥글을 시각적으로 구분하는 데 사용할 수 있는 테두리. </p> </td> 
  </tr> 
 </tbody> 
</table>

바닥글에는 단추를 유지하는 내부 컨테이너가 있습니다. 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogbuttoncontainer
```

대화 상자 단추 컨테이너의 **CSS 속성**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 바닥글과 단추 사이의 내부 패딩입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

모두 선택 단추는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogactionbutton
```

버튼은 데스크탑 시스템에서만 사용할 수 있습니다.

**모두 선택 단추의 CSS 속성**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
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
>모두 선택 단추는 `state` 특성 선택기를 지원하며, 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

취소 단추는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogcancelbutton
```

대화 상자 취소 단추의 **CSS 속성**

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
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
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
>취소 단추는 `state` 특성 선택기를 지원하며, 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

또한 두 버튼은 다른 대화 상자 버튼에 대해 동일한 CSS 설정을 포함할 수 있는 공통 CSS 클래스를 공유합니다.

```
.s7videoviewer .s7embeddialog .s7dialogfooter .s7button
```

**단추의 CSS 속성**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 모음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 줄 높이 </span> </p> </td> 
   <td colname="col2"> <p> 단추 내부의 텍스트 높이입니다. 세로 정렬에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상자-그림자 </span> </p> </td> 
   <td colname="col2"> <p>그림자. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 단추 여백입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

버튼 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)를 참조하십시오.

예 - 64 x 34 취소 버튼이 있는 대화 상자 바닥글을 설정하려면 텍스트 색상과 배경색이 각 버튼 상태에 따라 다릅니다.

```
.s7videoviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

머리글과 바닥글 사이의 기본 대화 상자 영역에는 스크롤 가능한 대화 상자 컨텐츠와 오른쪽의 스크롤 패널이 있습니다. 모든 경우 구성 요소가 이 영역의 너비를 관리하지만 CSS에서는 이 영역을 설정할 수 없습니다. 기본 대화 상자 영역은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogviewarea
```

**대화 상자 보기 영역의 CSS **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p> 기본 대화 상자 영역의 높이입니다. 대화 상자가 데스크탑 모드에서 작동하는 경우에만 지정해야 합니다. 대화 상자의 크기가 전체 브라우저 창을 차지하도록 설정되어 있는 경우에는 적용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>기본 대화 상자 영역의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 </span> </p> </td> 
   <td colname="col2"> <p>외부 여백. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 기본 대화 상자 영역을 300픽셀 높이로 설정하려면 10픽셀 여백을 사용하고 흰색 배경을 사용합니다.

```
.s7videoviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

모든 양식 콘텐츠(레이블 및 입력 필드 등)는 로 제어되는 컨테이너 내에 있습니다.

```
.s7videoviewer .s7embeddialog .s7dialogbody
```

이 컨테이너의 높이가 기본 대화 상자 영역보다 큰 경우 구성 요소에서 자동으로 세로 스크롤을 활성화합니다.

**대화 상자 본문의 CSS **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 10픽셀 패딩을 갖도록 양식 콘텐츠를 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

대화 상자 양식의 모든 정적 레이블은

```
.s7videoviewer .s7embeddialog .s7dialoglabel
```

이 클래스는 양식 사용자 인터페이스의 여러 위치에 있는 텍스트에 적용할 수 있으므로 레이블 크기나 위치를 제어하기에 적합하지 않습니다.

**대화 상자 레이블의 CSS 속성. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>레이블 글꼴 두께입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>레이블 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>레이블 글꼴 모음입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p>레이블 텍스트 색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

대화 상자 레이블 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)를 참조하십시오.

예 - 모든 레이블을 9픽셀 글꼴로 굵게, 회색으로 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

포함 코드 맨 위에 표시되는 텍스트 사본의 크기는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialoginputwide
```

대화 상자 입력 전체 필드의 **CSS 속성**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>입력 필드 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 텍스트 사본을 430픽셀 너비로 설정하고 아래쪽에 10픽셀 패딩이 있도록 하려면 다음을 수행하십시오.

```
.s7videoviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

포함 코드는 컨테이너에 래핑되고 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer
```

대화 상자 입력 컨테이너의 **CSS 속성**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>포함 코드 컨테이너의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 </span> </p> </td> 
   <td colname="col2"> <p>포함 코드 컨테이너 주위의 테두리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 포함 코드 텍스트 주위에 1픽셀 회색 테두리를 설정하려면 너비를 430픽셀로 만들고 10픽셀 패딩을 만듭니다.

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

실제 포함 코드 텍스트는 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer
```

대화 상자 입력 컨테이너의 **CSS 속성**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동 줄 바꿈 </span> </p> </td> 
   <td colname="col2"> <p>자동 줄바꿈 스타일입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 이 `break-word` 단어 줄바꿈을 사용하도록 포함된 코드를 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

포함 크기 레이블과 드롭다운은 대화 상자 하단에 있으며 다음 CSS 클래스 선택기로 제어되는 컨테이너에 삽입됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel
```

대화 상자 포함 크기 패널의 **CSS 속성**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 10픽셀의 패딩을 갖도록 포함 크기 패널을 설정하려면 다음 작업을 수행하십시오.

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

포함 크기 레이블의 크기 및 정렬은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel
```

대화 상자 포함 크기 패널의 **CSS 속성**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 수직 맞춤 </span> </p> </td> 
   <td colname="col2"> <p>세로 레이블 정렬. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>레이블 너비. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 포함 크기 레이블을 맨 위에 정렬하고 너비를 80픽셀로 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

포함 크기 콤보 상자의 너비는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7combobox
```

콤보 상자의 **CSS 속성**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>콤보 상자 폭. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>콤보 상자는 가능한 값 `true` 및 `false`이(가) 있는 `expanded` 특성 선택기를 지원합니다. `true` 값은 콤보 상자에 미리 정의된 포함 크기 중 하나가 표시되면 사용되므로 사용 가능한 모든 너비를 사용해야 합니다. `false` 값은 콤보 상자에서 사용자 지정 크기 옵션을 선택할 때 사용되므로 사용자 지정 너비 및 높이 입력 필드에 공백을 허용하도록 축소해야 합니다.

예 - 사전 정의된 항목을 표시할 경우 포함 크기 콤보 상자의 너비를 300픽셀로 설정하고 사용자 지정 크기를 표시할 경우 110픽셀로 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7videoviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

콤보 상자 텍스트의 높이는 특수 내부 요소에 의해 정의되며 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxtext
```

콤보 상자 텍스트의 **CSS 속성**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>콤보 상자 텍스트 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 포함 크기 콤보 상자 텍스트 높이를 40픽셀로 설정하려면:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

콤보 상자의 오른쪽에는 &quot;드롭다운&quot; 단추가 있으며, 이 단추는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

콤보 상자 단추의 **CSS 속성**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p>콤보 상자 안의 세로 단추 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>콤보 상자 안의 가로 단추 위치입니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>각 상태에 대한 단추 이미지. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

이 단추는 `state` 특성 선택기를 지원하며, 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

예 - &quot;드롭다운&quot; 단추를 28 x 28픽셀로 설정하고 각 상태에 대한 별도의 이미지를 보유하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

콤보 상자를 열 때 포함 크기 목록이 표시되는 패널은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7comboboxdropdown
```

패널의 크기와 위치는 구성 요소에 의해 제어됩니다. CSS를 통해 변경할 수 없습니다.

콤보 상자 드롭다운의 **CSS 속성**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 </span> </p> </td> 
   <td colname="col2"> <p>패널 테두리. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 콤보 상자 패널에 1픽셀 회색 테두리를 설정하려면:

```
.s7videoviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

다음 CSS 클래스 선택기로 제어되는 드롭다운 패널의 단일 항목:

```
.s7videoviewer .s7embeddialog .s7dropdownitemanchor
```

**드롭다운 항목 앵커의 CSS 속성**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>항목 배경입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 콤보 상자 패널 항목을 흰색 배경으로 설정하려면:

```
.s7videoviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

다음 CSS 클래스 선택기로 제어되는 콤보 상자 패널 내에서 선택한 항목의 왼쪽에 표시되는 확인 표시입니다.

```
.s7videoviewer .s7embeddialog .s7checkmark
```

**확인 표시 상자의 CSS 속성**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>항목 이미지. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 확인 표시 아이콘을 25 x 25픽셀로 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

포함 크기 콤보 상자에서 &quot;사용자 지정 크기&quot; 옵션을 선택하면 대화 상자의 오른쪽에 사용자 지정 포함 크기를 입력할 수 있는 두 개의 추가 입력 필드가 표시됩니다. 이러한 필드는 다음 CSS 클래스 선택기로 제어되는 컨테이너에서 래핑됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogcustomsizepanel
```

대화 상자 사용자 지정 크기 패널의 **CSS 속성**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 남음 </span> </p> </td> 
   <td colname="col2"> <p> 포함 크기 콤보 상자로부터의 거리입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 사용자 지정 크기 입력 필드 패널을 콤보 상자의 오른쪽에 20픽셀로 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

각 사용자 지정 크기 입력 필드는 테두리를 렌더링하고 필드 간의 여백을 설정하는 컨테이너에 래핑됩니다. 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogcustomsize
```

대화 상자 사용자 지정 크기의 **CSS 속성**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 </span> </p> </td> 
   <td colname="col2"> <p>입력 필드 주변의 테두리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 입력 필드 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 </span> </p> </td> 
   <td colname="col2"> <p> 입력 필드 여백. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 필드 패딩 입력. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 사용자 지정 크기 입력 필드를 회색 테두리, 여백, 패딩이 1픽셀이고 너비가 70픽셀이 되도록 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

수직 스크롤이 필요한 경우, 스크롤 막대가 대화 상자의 오른쪽 가장자리 부근 패널에 렌더링되며, 이 패널은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7dialogscrollpanel
```

대화 상자 스크롤 패널의 **CSS 속성**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>패널 폭을 스크롤합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 스크롤 패널을 44픽셀 너비로 설정합니다.

```
.s7videoviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

다음 CSS 클래스 선택기를 사용하여 스크롤 막대 영역의 모양이 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7scrollbar
```

**스크롤 막대의 CSS 속성**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 막대 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 패널의 위쪽에서 오프셋된 세로 스크롤 막대입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 패널 아래쪽에서 오프셋된 세로 스크롤 막대입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 패널의 오른쪽 가장자리에서 오프셋된 가로 스크롤 막대 </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 스크롤 패널의 위쪽, 오른쪽, 아래쪽에서 너비가 28픽셀이고 여백이 8픽셀인 스크롤 막대를 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

스크롤 막대 트랙은 위쪽 및 아래쪽 스크롤 단추 사이의 영역입니다. 이 구성 요소는 트랙의 위치와 높이를 자동으로 설정합니다. 트랙은 다음 CSS 클래스 선택기로 제어됩니다

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

스크롤 막대 트랙의 **CSS 속성**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>트랙 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 배경색을 추적합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 28픽셀 너비와 회색 배경을 가진 스크롤 막대 트랙을 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

스크롤 막대 썸네일이 스크롤 트랙 영역 내에서 세로로 이동합니다. 수직 위치는 구성 요소 로직에 의해 완전히 제어됩니다. 그러나 썸네일 높이는 컨텐츠의 양에 따라 동적으로 변경되지 않습니다. 다음 CSS 클래스 선택기를 사용하여 썸네일 높이 및 기타 측면을 구성할 수 있습니다.

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

스크롤 막대 썸네일의 **CSS 속성**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>썸네일 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>엄지손가락 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 상단 </span> </p> </td> 
   <td colname="col2"> <p>트랙 상단 사이의 수직 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩-하단 </span> </p> </td> 
   <td colname="col2"> <p> 트랙 하단 사이의 수직 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 지정된 썸네일 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb은 `state` 특성 선택기를 지원하며, 이 선택기는 다른 Thumb 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. `up`, `down`, `over` 및 `disabled`.

예 - 28 x 45픽셀이고 위쪽과 아래쪽에 10픽셀 여백이 있으며 각 상태에 대해 서로 다른 아트웍이 있는 스크롤 막대 썸을 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

다음 CSS 클래스 선택기를 사용하여 위쪽 및 아래쪽 스크롤 단추의 모양이 제어됩니다.

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton 
```

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

CSS 위쪽, 왼쪽, 아래쪽 및 오른쪽 속성을 사용하여 스크롤 단추를 배치할 수 없습니다. 대신 뷰어 로직이 자동으로 배치합니다.

**위쪽 및 아래쪽 스크롤 단추의 CSS 속성**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 지정된 버튼 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이러한 단추는 `state` 특성 선택기를 지원하며, 이 선택기는 `up`, `down`, `over` 및 `disabled` 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

버튼 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)를 참조하십시오.

예 - 28 x 32픽셀이며 각 상태에 대해 서로 다른 아트웍이 있는 스크롤 단추를 설정하려면 다음을 수행합니다.

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
