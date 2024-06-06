---
title: 링크 공유
description: 링크 공유 도구는 소셜 공유 패널에 추가된 버튼과 도구가 활성화될 때 표시되는 모달 대화 상자로 구성됩니다. 버튼의 위치는 소셜 공유 도구에서 완전히 관리됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 638ca6c2-375c-4162-b640-68aed6a8a9c6
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# 링크 공유{#link-share}

링크 공유 도구는 소셜 공유 패널에 추가된 버튼과 도구가 활성화될 때 표시되는 모달 대화 상자로 구성됩니다. 버튼의 위치는 소셜 공유 도구에서 완전히 관리됩니다.

<!--RICK - Edit to distinguish from previous -->

링크 공유 버튼의 모양은 다음 CSS 클래스 선택기로 제어합니다.

```css{.line-numbers}
.s7video360viewer .s7linkshare
```

**링크 공유 도구의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 폭 </span> </p> </td> 
   <td colname="col2"> <p>단추 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기: 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

을 설정하여 소셜 공유 패널에서 버튼을 제거할 수 있습니다 `display:none` CSS 클래스의 CSS 속성입니다.

단추 도구 설명을 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

예 - 28 x 28픽셀이고 네 개의 서로 다른 버튼 상태에 대해 각각 다른 이미지를 표시하는 링크 공유 단추를 설정하려면 다음을 수행합니다.

```css {.line-numbers}
.s7video360viewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7video360viewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7video360viewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7video360viewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

활성 대화 상자가 다음 CSS 클래스 선택기로 제어될 때 웹 페이지를 덮는 배경 오버레이:

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7backoverlay
```

**배경 오버레이의 CSS 속성**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도 </span> </p> </td> 
   <td colname="col2"> <p>배경 오버레이 불투명도. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>배경 오버레이 색상. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 배경 오버레이를 불투명도가 70%인 회색으로 설정하려면 다음을 수행합니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

기본적으로 모달 대화 상자는 데스크탑 시스템에서 화면 중앙에 표시되며 터치 디바이스에서 전체 웹 페이지 영역을 가져옵니다. 모든 경우 대화 상자의 위치 지정 및 크기 조정은 구성 요소에 의해 관리됩니다. 이 대화 상자는 다음 CSS 클래스 선택기로 제어됩니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialog
```

**대화 상자의 CSS 속성**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 대화 상자가 전체 브라우저를 사용하지 않는 경우 대화 상자 테두리 반경입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>대화 상자 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 폭 </span> </p> </td> 
   <td colname="col2"> <p>를 설정 해제하거나 100%로 설정해야 합니다. 이 경우 대화 상자는 전체 브라우저 창을 사용합니다(이 모드는 터치 장치에서 선호됨). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>를 설정 해제하거나 100%로 설정해야 합니다. 이 경우 대화 상자는 전체 브라우저 창을 사용합니다(이 모드는 터치 장치에서 선호됨). </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 전체 브라우저 창을 사용하고 터치 장치에 흰색 배경을 포함하도록 대화 상자를 설정하려면 다음을 수행하십시오.

```css {.line-numbers}
.s7video360viewer.s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

대화 상자 머리글은 아이콘, 제목 텍스트 및 닫기 단추로 구성됩니다. 헤더 컨테이너는 다음 CSS 클래스 선택기로 제어됩니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheader
```

**대화 상자 헤더의 CSS 속성**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 헤더 콘텐츠에 대한 내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

아이콘과 제목 텍스트는 다음 CSS 클래스 선택기로 제어되는 추가 컨테이너에 래핑됩니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline
```

**대화 상자 라인의 CSS 속성**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 헤더 아이콘 및 제목의 내부 패딩 </p> </td> 
  </tr> 
 </tbody> 
</table>

헤더 아이콘은 다음 CSS 클래스 선택기로 제어됩니다

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheadericon
```

**대화 상자 헤더 아이콘의 CSS 속성**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 폭 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>아이콘 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>아이콘 이미지 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

헤더 제목은 다음 CSS 클래스 선택기로 제어됩니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheadertext
```

**대화 상자 헤더 텍스트의 CSS 속성**

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

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7closebutton
```

**닫기 버튼의 CSS 속성**

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> 머리글 컨테이너를 기준으로 한 세로 단추 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 헤더 컨테이너를 기준으로 한 가로 단추 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 폭 </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>각 상태에 대한 단추 이미지. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기: 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

닫기 단추 도구 팁과 대화 상자 제목을 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**예** - 패딩이 있는 대화 상자 헤더를 설정하려면 22x12픽셀 아이콘과 굵은 16포인트 제목을 설정합니다. 그리고 마지막으로 대화 상자 컨테이너의 위쪽에서 2픽셀, 오른쪽에서 2픽셀에 각각 배치된 28x28픽셀 닫기 단추입니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

대화 상자 바닥글은 취소 단추로 구성됩니다. 바닥글 컨테이너는 다음 CSS 클래스 선택기로 제어됩니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogfooter
```

**대화 상자 바닥글의 CSS 속성**

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 </span> </p> </td> 
   <td colname="col2"> <p> 대화 상자의 나머지 부분과 바닥글을 시각적으로 구분하는 데 사용할 수 있는 테두리. </p> </td> 
  </tr> 
 </tbody> 
</table>

바닥글에는 단추를 유지하는 내부 컨테이너가 있습니다. 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer
```

**대화 상자 버튼 컨테이너의 CSS 속성**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 바닥글과 단추 사이의 내부 패딩입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

모두 선택 단추는 다음 CSS 클래스 선택기로 제어됩니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogactionbutton
```

버튼은 데스크탑 시스템에서만 사용할 수 있습니다.

**모두 선택 단추의 CSS 속성**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 폭 </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 각 상태에 대한 단추 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>모두 선택 단추는 `state` 속성 선택기: 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

취소 단추는 다음 CSS 클래스 선택기로 제어됩니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogcancelbutton
```

**대화 상자의 CSS 속성 취소 단추**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 폭 </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 각 상태에 대한 단추 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기: 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

또한 두 버튼은 다른 대화 상자 버튼에 대해 동일한 CSS 설정을 포함할 수 있는 공통 CSS 클래스를 공유합니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button
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
   <td colname="col1"> <p> <span class="codeph"> 선 높이 </span> </p> </td> 
   <td colname="col2"> <p> 단추 내부의 텍스트 높이입니다. 세로 정렬에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상자 그림자 </span> </p> </td> 
   <td colname="col2"> <p>그림자. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 여백 </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 단추 여백입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

버튼 도구 팁은 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**예** - 64 x 34 취소 버튼이 있는 대화 상자 바닥글을 설정하려면 텍스트 색상과 배경색이 각 버튼 상태에 따라 다릅니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

머리글과 바닥글 사이의 기본 대화 상자 영역에는 대화 상자 내용이 포함됩니다. 모든 경우 구성 요소는 이 영역의 너비를 관리합니다. CSS에서는 이 영역을 설정할 수 없습니다. 기본 대화 상자 영역은 다음 CSS 클래스 선택기로 제어됩니다.

```css{.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogviewarea
```

**대화 상자 보기 영역의 CSS 속성**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p> 기본 대화 상자 영역의 높이입니다. 대화 상자가 데스크탑 모드에서 작동하는 경우에만 지정해야 합니다. 대화 상자의 크기가 전체 브라우저 창을 차지하도록 설정되어 있는 경우에는 적용할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>기본 대화 상자 영역의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 </span> </p> </td> 
   <td colname="col2"> <p>외부 여백. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 기본 대화 상자 영역을 300픽셀 높이로 설정하고 10픽셀 여백을 두며 흰색 배경을 사용합니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

레이블 및 입력 필드와 같은 모든 양식 콘텐츠는 다음 CSS 클래스 선택기로 제어되는 컨테이너 내에 있습니다.

```css{.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogbody
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

**예** - 10픽셀 패딩을 갖도록 양식 콘텐츠를 설정하려면 다음을 수행합니다.

```css {.line-numbers}
.s7interactivevideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

대화 상자 양식의 모든 정적 레이블은

```
.s7video360viewer .s7linkdialog .s7dialoglabel
```

이 클래스는 양식 사용자 인터페이스의 여러 위치에 있는 텍스트에 적용할 수 있으므로 레이블 크기나 위치를 제어하기에 적합하지 않습니다.

**대화 상자 레이블의 CSS 속성**

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
   <td colname="col1"> <p> <span class="codeph"> 색상 </span> </p> </td> 
   <td colname="col2"> <p>레이블 텍스트 색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

대화 상자 레이블을 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**예** - 모든 레이블을 9픽셀 글꼴로 굵게 회색으로 설정하려면 다음을 수행합니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

링크 위에 표시되는 텍스트 사본의 크기는 다음 CSS 클래스 선택기로 제어합니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputwide
```

**대화 상자 입력 범위 필드의 CSS 속성**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 폭 </span> </p> </td> 
   <td colname="col2"> <p>텍스트 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 텍스트 사본을 430픽셀 너비로 설정하고 아래쪽에 10픽셀 패딩이 있도록 하려면 다음을 수행하십시오.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

공유 링크는 컨테이너로 래핑되고 다음 CSS 클래스 선택기로 제어됩니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputcontainer
```

**대화 상자 입력 컨테이너의 CSS 속성**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 </span> </p> </td> 
   <td colname="col2"> <p>공유 링크 컨테이너 주변의 테두리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 포함 코드 텍스트 주위에 1픽셀 회색 테두리를 설정하고 9픽셀 패딩을 포함하려면 다음을 수행하십시오.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

공유 링크 자체는 다음 CSS 클래스 선택기로 제어됩니다.

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoglink
```

**대화 상자 공유 링크의 CSS 속성**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 폭 </span> </p> </td> 
   <td colname="col2"> <p>링크 너비 공유. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 공유 링크를 450픽셀 너비로 설정하려면 다음을 수행합니다.

```css{.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```
