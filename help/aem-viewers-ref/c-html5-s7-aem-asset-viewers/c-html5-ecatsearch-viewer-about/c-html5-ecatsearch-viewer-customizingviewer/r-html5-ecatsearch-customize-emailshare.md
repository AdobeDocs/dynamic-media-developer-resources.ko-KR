---
description: 이메일 공유 도구는 도구를 활성화하면 표시되는 모달 대화 상자와 소셜 공유 패널에 추가된 단추로 구성됩니다. 단추의 위치는 소셜 공유 도구에 의해 완전히 관리됩니다.
seo-description: 이메일 공유 도구는 도구를 활성화하면 표시되는 모달 대화 상자와 소셜 공유 패널에 추가된 단추로 구성됩니다. 단추의 위치는 소셜 공유 도구에 의해 완전히 관리됩니다.
seo-title: 이메일 공유
solution: Experience Manager
title: 이메일 공유
uuid: fc60dd7b-651e-458c-9057-693ca1c0afdc
feature: Dynamic Media Classic,뷰어,SDK/API,eCatalog 검색
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '3084'
ht-degree: 1%

---


# 전자 메일 공유{#email-share}

이메일 공유 도구는 도구를 활성화하면 표시되는 모달 대화 상자와 소셜 공유 패널에 추가된 단추로 구성됩니다. 단추의 위치는 소셜 공유 도구에 의해 완전히 관리됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

이메일 공유 버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emailshare
```

**이메일 공유 도구의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>단추의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

CSS 클래스에서 `display:none` CSS 속성을 설정하여 소셜 공유 패널에서 단추를 제거할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 28 x 28픽셀인 전자 메일 공유 단추를 설정하고 서로 다른 4개의 단추 상태 각각에 대해 다른 이미지를 표시하는 경우

```
.s7ecatalogsearchviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

대화 상자가 활성 상태일 때 웹 페이지를 덮는 배경 오버레이는 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay
```

**뒤로 오버레이의 CSS 속성**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 불투명도  </span> </p> </td> 
   <td colname="col2"> <p> 배경 오버레이 불투명도. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>배경 오버레이 색상. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 70%의 불투명도를 사용하여 회색으로 배경 오버레이를 설정하려면:

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

기본적으로 모달 대화 상자는 데스크톱 시스템의 화면에 중앙에 표시되며 터치 장치에서 전체 웹 페이지 영역을 가져옵니다. 모든 경우 대화 상자의 위치 지정 및 크기는 구성 요소에 의해 관리됩니다. 대화 상자는 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialog
```

**대화 상자의 CSS 속성**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> 대화 상자 테두리 반경(대화 상자에서 전체 브라우저 창을 사용하지 않는 경우); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 대화 상자 배경색; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p> 설정이 해제되거나 100%로 설정되어야 합니다. 이 경우 대화 상자가 전체 브라우저 창을 사용합니다(이 모드는 터치 장치에서 기본 설정). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> 설정이 해제되거나 100%로 설정되어야 합니다. 이 경우 대화 상자가 전체 브라우저 창을 사용합니다(이 모드는 터치 장치에서 기본 설정). </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 터치 장치에 흰색 배경이 있고 전체 브라우저 창을 사용하도록 대화 상자를 설정하려면:

```
.s7ecatalogsearchviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

대화 상자 헤더는 아이콘, 제목 텍스트 및 닫기 단추로 구성됩니다. 헤더 컨테이너는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader
```

**대화 상자 헤더의 CSS 속성**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 머리글 컨텐츠에 대한 내부 패딩입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

아이콘 및 제목 텍스트는

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**대화 상자의 CSS 속성**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 머리글 아이콘 및 제목의 내부 패딩입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

머리글 아이콘은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon
```

**대화 상자 머리글 아이콘의 CSS 속성**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>아이콘 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>아이콘 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>아이콘 이미지. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

머리글 제목은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext
```

**대화 상자 머리글 텍스트의 CSS 속성**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 모음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 텍스트 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

닫기 버튼은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton
```

**닫기 단추의 CSS 속성 **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p> 머리글 컨테이너를 기준으로 하는 세로 단추 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 머리글 컨테이너를 기준으로 하는 가로 단추 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>단추 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>단추의 내부 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>각 상태에 대한 단추 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

닫기 단추 도구 팁과 대화 상자 제목을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 패딩, 24 x 17픽셀 아이콘, 굵은 16포인트 제목, 28 x 28픽셀 닫기 단추 등의 대화 상자 컨테이너 오른쪽에 2픽셀과 대화 상자 컨테이너의 오른쪽에서 2픽셀을 배치하여 대화 상자 헤더를 설정하려면:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

대화 상자 바닥글은 [취소] 및 [이메일 보내기] 단추로 구성됩니다. 바닥글 컨테이너는 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter
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

바닥글에는 두 단추를 모두 유지하는 내부 컨테이너가 있습니다. 이 컨트롤은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer
```

**대화 상자 단추 컨테이너의 CSS 속성**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p> 바닥글과 단추 사이의 내부 패딩입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

취소 버튼은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton
```

**대화 상자 취소 단추의 CSS 속성**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>단추 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 각 상태에 대한 단추 텍스트 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 각 상태에 대한 단추 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

이메일 보내기 단추는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton
```

**대화 상자 작업 단추의 CSS 속성**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>단추 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> 각 상태에 대한 단추 텍스트 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 각 상태에 대한 단추 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

또한 두 버튼은 다른 대화 상자 버튼과 동일한 CSS 설정을 포함할 수 있는 동일한 공통 CSS 클래스를 공유합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button
```

**버튼의 CSS 속성**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께  </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 모음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 선 높이  </span> </p> </td> 
   <td colname="col2"> <p> 단추 안의 텍스트 높이. 세로 정렬에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상자 그림자  </span> </p> </td> 
   <td colname="col2"> <p>그림자 효과. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 여백  </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 단추 여백. </p> </td> 
  </tr> 
 </tbody> 
</table>

이 단추 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 각 단추 상태에 대해 텍스트 색상과 배경색이 다른 64 x 34 [취소] 단추 및 82 x 34 [이메일 보내기] 단추와 함께 대화 상자 바닥글을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

머리글과 바닥글 사이의 기본 대화 상자 영역에는 스크롤 가능한 대화 상자 내용과 오른쪽의 스크롤 패널이 있습니다. 모든 경우 구성 요소는 이 영역의 너비를 관리하므로 CSS로 설정할 수 없습니다. 기본 대화 상자 영역은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea
```

**대화 상자 보기 영역의 CSS 속성 **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> 기본 대화 상자 영역의 높이입니다. 대화 상자가 데스크탑 모드에서 작동하는 경우에만 이 대화 상자를 지정해야 합니다. 대화 상자의 크기가 전체 브라우저 창을 차지하도록 지정된 경우에는 적용되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>기본 대화 상자 영역의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>외부 여백입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>기본 대화 상자 영역은 선택적 `state` 속성 선택기를 지원합니다. 이메일 양식이 전송되고 대화 상자에 확인 메시지가 표시되면 이 메시지가 `sendsuccess`으로 설정됩니다. 확인 메시지가 작은 한 이 속성 선택기를 사용하여 확인 메시지가 표시될 때 대화 상자 높이를 줄일 수 있습니다.

예 - 확인 메시지가 표시될 때 기본 대화 상자 영역을 처음에 300픽셀 높이 및 100픽셀 높이로 설정하려면 10픽셀 여백을 사용하고 흰색 배경을 사용합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

모든 양식 컨텐츠(예: 레이블 및 입력 필드)는 다음 CSS 클래스 선택기로 제어되는 컨테이너 내에 있습니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody
```

이 컨테이너의 높이가 기본 대화 상자 영역보다 큰 것으로 나타나면 구성 요소에 의해 자동으로 세로 스크롤이 활성화됩니다.

**대화 상자 본문의 CSS 속성 **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 10픽셀 패딩이 있도록 양식 컨텐츠를 설정하려면:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

대화 상자 양식은 라인별로 채워져 있으며 각 라인은 양식 컨텐츠의 일부(레이블 및 텍스트 입력 필드 등)를 전달합니다. 단일 폼 라인은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**대화 상자 줄의 CSS 속성**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 줄 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 각 줄에 10픽셀 패딩이 있도록 대화 상자 양식을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

대화 상자 양식의 모든 정적 레이블은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel
```

이 클래스는 양식 사용자 인터페이스의 다양한 위치에 있는 텍스트에 적용할 수 있으므로 레이블 크기 또는 위치를 제어하는 데 적합하지 않습니다.

**대화 상자 레이블의 CSS 속성입니다. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께  </span> </p> </td> 
   <td colname="col2"> <p>레이블 글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>레이블 글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 모음 레이블을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상에 레이블을 지정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

대화 상자 레이블은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 9픽셀 글꼴로 모든 레이블을 회색, 굵게 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

양식 입력 필드 왼쪽에 표시되는 모든 정적 레이블은 다음과 같이 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel
```

**대화 상자 입력 레이블의 CSS 속성**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>정적 레이블의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>가로 텍스트 정렬입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>정적 레이블 여백. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>정적 레이블 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 입력 필드 레이블을 50픽셀 너비, 오른쪽 정렬로 설정하려면 패딩 10픽셀, 오른쪽에 10픽셀 여백을 설정합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

각 양식 입력 필드는 입력 필드 주위에 사용자 정의 테두리를 적용할 수 있도록 컨테이너로 둘러싸여 있습니다. 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer
```

**대화 상자 입력 컨테이너의 CSS 속성**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>입력 필드 컨테이너 주위의 테두리 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>입력 필드 컨테이너는 선택적 `state` 속성 선택기를 지원합니다. 사용자가 입력 데이터 형식을 잘못하고 인라인 유효성 검사에 실패하는 경우 이 값은 `verifyerror`으로 설정됩니다. 이 속성 선택기를 사용하여 양식에서 잘못된 사용자 입력을 강조 표시할 수 있습니다.

대화 상자 본문의 오른쪽 가장자리(시작 필드 및 메시지 필드 포함)에 대한 레이블에서 스프레드되는 대부분의 입력 필드는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide
```

**대화 상자의 CSS 속성 입력 전체 필드**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>입력 필드 너비. </p> </td> 
  </tr> 
 </tbody> 
</table>

받는 사람 필드는 오른쪽의 [이메일 제거] 단추에 대한 공간을 할당하므로 더 좁습니다. 이 컨트롤은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort
```

**대화 상자 입력 짧은 필드의 CSS 속성**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>입력 필드 너비. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 모든 입력 필드 주위에 패딩이 9픽셀인 1픽셀 회색 테두리가 있는 양식을 설정하려면유효성 검사가 실패한 필드에 대해 동일한 테두리를 빨간색 색상으로 설정하고, 폭 250픽셀인 [끝] 필드 및 나머지 입력 필드의 너비가 300픽셀인 경우:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

이메일 메시지 입력 필드는 다음으로 추가로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage
```

이 클래스를 사용하면 기본 `TEXTAREA` 요소에 대한 특정 속성을 설정할 수 있습니다.

**대화 상자 메시지의 CSS 속성**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>메시지 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap  </span> </p> </td> 
   <td colname="col2"> <p>Word 줄바꿈 스타일입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 이메일 메시지를 50픽셀 높이로 설정하고 `break-word` 줄 바꿈을 사용하려면:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

[다른 이메일 주소 추가] 단추를 사용하면 사용자가 이메일 양식에 수신자를 두 명 이상 추가할 수 있습니다. 이 컨트롤은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton
```

**대화 상자의 CSS 속성 추가 이메일 주소 단추**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>각 상태에 대한 단추 텍스트 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>각 상태에 대한 단추 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p>단추 영역 내의 단추 이미지 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께  </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>단추 글꼴 모음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 선 높이  </span> </p> </td> 
   <td colname="col2"> <p>단추 안의 텍스트 높이. 세로 정렬에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>가로 텍스트 정렬. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - &quot;다른 이메일 주소 추가&quot; 단추를 25픽셀 높이로 설정하려면 오른쪽 정렬의 12포인트 굵은 글꼴 및 각 상태에 대해 다른 텍스트 색상 및 이미지를 사용합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

제거 단추를 사용하면 사용자가 이메일 양식에서 추가 주소를 제거할 수 있습니다. 이 컨트롤은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton
```

**대화 상자의 CSS 속성: 이메일 제거 단추**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>단추 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>각 상태에 대한 단추 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 제거 단추를 25 x 25픽셀로 설정하고 각 상태에 대해 다른 이미지를 사용하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

공유 중인 컨텐츠는 대화 상자 본문의 하단에 표시되며 축소판, 제목, 원본 URL 및 설명이 포함되어 있습니다. 컨테이너는 다음 CSS 클래스 선택기로 제어되는 컨테이너로 래핑됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**대화 상자 내용의 CSS 속성 **

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>컨테이너 테두리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 아래쪽 컨테이너를 설정하여 1픽셀 점선 테두리와 패딩이 없는 경우:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

축소판 이미지는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail
```

`background-image` 속성은 구성 요소 논리로 설정됩니다.

**대화 상자 축소판 이미지의 CSS 속성**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>축소판 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>축소판 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 수직 정렬  </span> </p> </td> 
   <td colname="col2"> <p>세로 정렬 축소판. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 축소판을 90 x 60픽셀로 설정하고 10픽셀의 패딩과 맨 위에 정렬하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

내용 제목, 원본 및 설명은 컨텐츠 축소판 오른쪽에 있는 패널로 추가로 그룹화됩니다. 이 컨트롤은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel
```

**대화 상자 정보 패널의 CSS 속성**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>패널 너비. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 컨텐츠 정보 패널을 너비 300픽셀로 설정하려면:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

콘텐츠 제목은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle
```

**대화 상자 제목의 CSS 속성**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>외부 여백입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 모음. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 굵은 글꼴을 사용하고 10픽셀 여백을 포함하도록 컨텐츠 제목을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

내용 원점은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin
```

**대화 상자 내용 원본의 CSS 속성 **

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>외부 여백입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 모음. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 내용 원점을 10픽셀 여백이 되도록 설정하려면:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

내용 설명은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription
```

**대화 상자 내용 설명의 CSS 속성**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>외부 여백입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 모음. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 내용 설명을 설정하여 10픽셀 여백을 사용하고 9포인트 글꼴을 사용합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

사용자가 잘못된 입력 데이터를 입력하고 인라인 유효성 검사가 실패하거나, 양식이 제출될 때 대화 상자에서 오류 또는 확인 메시지를 렌더링해야 할 때 대화 상자 본문 맨 위에 메시지가 표시됩니다. 이 컨트롤은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage
```

**대화 상자 오류 메시지의 CSS 속성**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> 오류 아이콘. 기본값은 느낌표입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> 메시지 영역 내의 오류 아이콘 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>메시지 텍스트 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 모음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 선 높이  </span> </p> </td> 
   <td colname="col2"> <p> 메시지 내의 텍스트 높이. 세로 정렬에 영향을 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 메시지는 다음 가능한 값으로 `state` 속성 선택기를 지원합니다.`verifyerror`, `senderror` 및 `sendsuccess`. `verifyerror` 은 인라인 입력 유효성 검사 오류로 인해 메시지가 표시될 때 설정됩니다. `senderror` 은 백엔드 이메일 서비스가 오류를 보고할 때 설정됩니다. `sendsuccess` 가 설정된 경우에만 유효합니다. 이렇게 하면 대화 상자 상태에 따라 메시지의 스타일을 다르게 지정할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 10포인트 굵은 글꼴을 사용하도록 메시지를 설정하려면 25픽셀 선 높이, 왼쪽에 20픽셀 패딩, 느낌표 아이콘, 오류 발생 시 빨간색 텍스트를 사용하고 성공 시 아이콘과 녹색 텍스트가 없는 경우 다음과 같이 하십시오.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

세로 스크롤이 필요한 경우 스크롤 막대가 대화 상자의 오른쪽 가장자리 근처에 있는 패널에서 렌더링되며, 이 패널은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel
```

**대화 상자 스크롤 패널의 CSS 속성**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>스크롤 패널 너비. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 스크롤 패널을 너비 44픽셀로 설정하려면:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

스크롤 막대 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar
```

**스크롤 막대의 CSS 속성**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 막대 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 패널 위쪽에서 세로 스크롤 막대 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 패널 아래쪽에서 세로 스크롤 막대 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 패널의 오른쪽 가장자리에서 수평 스크롤 막대 오프셋입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 스크롤 패널의 위쪽, 오른쪽 및 아래쪽에서 28픽셀의 스크롤 막대를 설정하고 8픽셀의 여백을 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

스크롤 막대 트랙은 위쪽 및 아래쪽 스크롤 단추 사이의 영역입니다. 구성 요소는 트랙의 위치와 높이를 자동으로 설정합니다. 트랙은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**스크롤 트랙의 CSS 속성**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>트랙 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>트랙 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 폭이 28픽셀이고 배경이 회색인 스크롤 막대 트랙을 설정하려면 다음과 같이 하십시오.

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

스크롤 막대 축소판 표시는 스크롤 트랙 영역 내에서 세로로 이동합니다. 세로 위치는 구성 요소 논리로 완전히 제어되지만 축소판 높이는 컨텐츠 양에 따라 동적으로 변경되지 않습니다. 다음 CSS 클래스 선택기를 사용하여 축소판 높이와 기타 측면을 구성할 수 있습니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**스크롤 막대 축소판 CSS 속성**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>축소판 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>엄지 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 위쪽  </span> </p> </td> 
   <td colname="col2"> <p> 트랙 위쪽 사이의 세로 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 하단  </span> </p> </td> 
   <td colname="col2"> <p> 트랙 아래쪽 사이의 세로 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>주어진 축소판 상태에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb는 다른 축소판 상태에 다른 스킨을 적용하는 데 사용할 수 있는 `state` 속성 선택기를 지원합니다.`up`, `down`, `over` 및 `disabled`.

예 - 28 x 45픽셀인 스크롤 막대 축소판 표시 및 위쪽과 아래쪽에 10픽셀 여백이 있고 각 상태에 대해 서로 다른 아트웍을 설정하는 방법은 다음과 같습니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

위쪽 및 아래쪽 스크롤 단추의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton
```

CSS `top`, `left`, `bottom` 및 `right` 속성을 사용하여 스크롤 단추를 배치할 수 없습니다. 대신 뷰어 논리는 자동으로 위치를 지정합니다.

**위쪽 및 아래쪽 스크롤 단추의 CSS 속성**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>단추 폭입니다. </p> </td> 
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
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이러한 단추는 `state` 속성 선택기를 지원하며, 이를 사용하여 서로 다른 단추 상태에 다른 스킨을 적용할 수 있습니다.`up`, `down`, `over` 및 `disabled`.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 28 x 32픽셀이고 각 상태에 대해 서로 다른 아트웍을 포함하는 스크롤 단추를 설정하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

