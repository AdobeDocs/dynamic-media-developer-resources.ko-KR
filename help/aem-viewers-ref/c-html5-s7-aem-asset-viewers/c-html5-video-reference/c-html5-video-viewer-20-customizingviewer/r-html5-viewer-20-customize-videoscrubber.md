---
title: 비디오 스크러버
description: 비디오 스크러버는 사용자가 현재 재생 중인 비디오 내의 모든 시간 위치를 동적으로 탐색할 수 있는 수평 슬라이더 컨트롤입니다
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 0%

---

# 비디오 스크러버{#video-scrubber}

비디오 스크러버는 사용자가 현재 재생 중인 비디오 내의 모든 시간 위치를 동적으로 찾을 수 있는 가로 슬라이더 컨트롤입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

비디오가 재생될 때 스크러버 &#39;손잡이&#39;도 움직여서 재생 중 비디오의 현재 시간 위치를 가리킨다. 비디오 스크러버는 항상 컨트롤 막대의 전체 너비를 사용합니다. CSS를 사용하여 비디오 스크러버의 스킨을 만들고 높이 및 세로 위치를 변경할 수 있습니다.

비디오 스크러버의 일반적인 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**비디오 스크러버의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 위쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 아래쪽 테두리에서 위치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버 색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 배경, 재생 및 로드 지표를 추적합니다.

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

트랙의 **CSS 속성**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>해당 트랙의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>해당 트랙의 색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 손잡이를 제어합니다.

```
.s7videoviewer .s7videoscrubber .s7knob
```

**노브의 CSS 속성**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p>세로 손잡이 오프셋. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>손잡이 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>손잡이 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>손잡이 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 재생된 시간 버블을 제어합니다.

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**재생된 시간의 CSS 속성**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> 시간에 사용할 글꼴 모음 표시 텍스트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>거품 영역 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>버블 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 텍스트 맞춤 </span> </p> </td> 
   <td colname="col2"> <p>텍스트를 버블 영역과 정렬합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

비디오 스크러버 도구 팁을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)를 참조하십시오.

**예** - 사용자 지정 트랙 색상으로 비디오 스크러버를 사용하여 비디오 뷰어를 설정합니다. 스크러버는 10픽셀이어야 하며, 컨트롤 막대의 위쪽 및 왼쪽 가장자리에서 10픽셀과 35픽셀을 배치해야 합니다.

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

`navigation` 매개 변수로 비디오 챕터를 활성화하면 챕터 위치가 비디오 스크러버 트랙 위에 마커로 표시됩니다.

비디오 챕터 마커는 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

비디오 챕터 마커의 **CSS 속성**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 마커 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 마커 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 마커 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 서로 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있는 `state` 특성 선택기를 모두 지원합니다. 특히 `selected='default'`은(는) 기본 비디오 챕터 마커 상태에 해당하며 `selected='over'`은(는) 마우스 오버 또는 터치 제스처로 비디오 챕터 마커가 활성화될 때 사용됩니다.

**예** - 5 x 8픽셀이고 &quot;기본&quot; 및 &quot;초과&quot; 상태에 다른 아트를 사용하는 비디오 챕터 마커를 설정합니다.

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

비디오 챕터 버블은 비디오 챕터 마커의 맨 위에 위치하며 지정된 챕터의 제목, 시작 시간 및 설명을 표시합니다. 비디오 스크러버 트랙에 대해 최대 버블 폭과 수직 오프셋을 제어할 수 있다. 나머지는 구성 요소에 의해 자동으로 계산됩니다.

비디오 챕터 버블은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**비디오 챕터 버블의 CSS 속성**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최대 너비 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 버블의 최대 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버 트랙에서의 수직 오프셋입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 비디오 스크러버 트랙의 맨 아래에서 8픽셀 위로 235픽셀 너비의 비디오 챕터 버블을 설정합니다.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

비디오 챕터 버블은 선택적 헤더와 콘텐츠로 구성됩니다. 헤더에는 선택적 챕터 시작 시간 및 챕터 제목이 있습니다.

헤더는 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**비디오 챕터 버블 헤더의 CSS 속성**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 버블 헤더 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 버블 헤더 텍스트에 대한 내부 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 버블 헤더 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 줄 높이 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 버블 헤더 텍스트 줄 높이. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 높이 22픽셀, 선 높이 22픽셀, 가로 여백 12픽셀 및 회색 배경인 비디오 챕터 버블 헤더를 설정하려면.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

비디오 챕터의 시작 시간은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**비디오 챕터 시작 시간의 CSS 속성**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 모음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 시작 시간과 챕터 제목 사이의 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 회색 10픽셀 Verdana 글꼴을 사용하여 챕터 시작 시간을 설정하려면 오른쪽에 10픽셀 패딩이 있습니다.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

비디오 챕터 제목은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**비디오 챕터 제목의 CSS 속성**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 제목 텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 제목 글꼴 두께입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 제목 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 제목 글꼴 모음 </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 흰색, 굵게, 10픽셀 Verdana 글꼴을 사용하는 비디오 챕터 제목을 설정합니다.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

비디오 챕터 설명은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

**비디오 챕터 설명의 CSS 속성**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 설명 텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 설명 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 설명 글꼴 두께입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 설명 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 설명 글꼴 모음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 줄 높이 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 설명 줄 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>비디오 챕터 설명 내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 밝은 회색 배경의 11픽셀 Verdana 글꼴을 사용하여 비디오 챕터 설명을 설정합니다. 마지막으로 에서는 5개의 픽셀 라인 높이, 12개의 픽셀 가로 패딩, 12개의 픽셀 위쪽 패딩 및 9개의 픽셀 아래쪽 패딩을 사용합니다.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

챕터 버블 아래쪽에 있는 웨지 커넥터는 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**쐐기 커넥터의 CSS 속성**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>쐐기 커넥터 색상. </p> <p>위쪽 테두리 색만 정의되고 나머지 테두리는 투명하게 남도록 <span class="codeph"> &lt;color&gt; 투명 </span>(으)로 정의됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 너비 </span> </p> </td> 
   <td colname="col2"> <p> 쐐기 커넥터 너비. </p> <p><span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span>(으)로 정의되므로 위쪽 및 가로 테두리에 대해서만 동일한 너비를 정의하며 아래쪽 테두리 너비는 <span class="codeph"> 0 </span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 </span> </p> </td> 
   <td colname="col2"> <p> 음수 하단 여백만 정의합니다. <span class="codeph"> border-width </span>과(와) 같은 값을 가져야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 회색 6픽셀 쐐기 커넥터를 설정하려면:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
