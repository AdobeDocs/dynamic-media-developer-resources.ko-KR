---
description: 비디오 스크러버는 사용자가 현재 재생 중인 비디오 내의 임의의 시간 위치를 동적으로 검색할 수 있도록 하는 수평 슬라이더 컨트롤입니다.
seo-description: 비디오 스크러버는 사용자가 현재 재생 중인 비디오 내의 임의의 시간 위치를 동적으로 검색할 수 있도록 하는 수평 슬라이더 컨트롤입니다.
seo-title: 비디오 스크러버
solution: Experience Manager
title: 비디오 스크러버
topic: Dynamic media
uuid: 5e4abc8a-ee61-4528-a5de-66148aac3389
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 2%

---


# 비디오 scrubber{#video-scrubber}

비디오 스크러버는 사용자가 현재 재생 중인 비디오 내의 임의의 시간 위치를 동적으로 검색할 수 있도록 하는 수평 슬라이더 컨트롤입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

또한 scrubber가 재생되는 동안 비디오의 현재 시간 위치를 나타내기 위해 비디오가 재생될 때 이동합니다. 비디오 스크러버는 항상 컨트롤 막대의 전체 폭을 사용합니다. 비디오 스크러버를 피울 수 있다. 높이와 세로 위치를 CSS로 변경합니다.

비디오 스크러버의 일반 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**비디오 스크러버의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩과 같이 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 패딩과 같이 아래쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버 색상입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 배경, 재생 및 로드 표시기를 추적합니다.

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**트랙의 CSS 속성**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>해당 트랙의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>해당 트랙의 색상입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 노브를 제어합니다.

```
.s7videoviewer .s7videoscrubber .s7knob
```

**노브의 CSS 속성**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>세로 노브 오프셋. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>노브의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>손잡이의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>아트웍을 조절합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 재생 버블 시간을 제어합니다.

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**재생된 버블 시간의 CSS 속성**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 모음입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>아트웍을 버블로 만듭니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>버블 영역과 텍스트 정렬 </p> </td> 
  </tr> 
 </tbody> 
</table>

비디오 스크러버 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)의 현지화를 참조하십시오.

**예**  - 높이 10픽셀이고 컨트롤 막대의 위쪽 및 왼쪽 가장자리에서 10픽셀 및 35픽셀의 사용자 정의 트랙 색상이 포함된 비디오 스크러버를 설정하려면

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

`navigation` 매개 변수를 사용하여 비디오 장 입력을 활성화하면 장 위치가 비디오 스크러버 트랙의 맨 위에 마커로 표시됩니다.

비디오 장 마커는 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

**비디오 장 마커의 CSS 속성**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 마커 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 마커 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 마커 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 모두 지원하므로 다른 버튼 상태에 다른 스킨을 적용할 수 있습니다. 특히, `selected='default'`은 기본 비디오 장 마커 상태에 해당하고 마우스 오버 또는 터치 제스처에 의해 비디오 장 마커가 활성화될 때 `selected='over'`이 사용됩니다.

**예**  - 5 x 8픽셀인 비디오 장 마커를 설정하고 &quot;기본값&quot; 및 &quot;오버&quot; 상태에 다른 아트를 사용하려면

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

비디오 장 버블은 비디오 장 마커의 맨 위에 배치되며 지정된 장의 제목, 시작 시간 및 설명을 표시합니다. 비디오 스크러버 트랙에 상대적인 최대 버블 폭과 세로 오프셋을 제어할 수 있습니다. 나머지 항목은 구성 요소에 의해 자동으로 계산됩니다.

비디오 장 버블은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**비디오 장 버블의 CSS 속성**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최대 폭  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블의 최대 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버 트랙의 수직 오프셋입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 비디오 스크러버 트랙의 아래쪽에서 8픽셀인 235픽셀의 비디오 장 버블을 설정하려면

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

비디오 장 버블은 선택적 헤더와 컨텐츠로 구성됩니다. 머리글에는 선택 사항으로 장 시작 시간과 장 제목이 있습니다.

헤더는 다음과 같은 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**비디오 장 버블 헤더의 CSS 속성**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 헤더 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 머리글 텍스트의 내부 패딩입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 헤더 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 선 높이  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 머리글 텍스트 줄 높이. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 22픽셀 높이, 22픽셀 선 높이, 12픽셀 가로 여백 및 회색 배경인 비디오 장 버블 헤더를 설정하려면

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

비디오 장의 시작 시간은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**비디오 장 시작 시간의 CSS 속성**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 패딩  </span> </p> </td> 
   <td colname="col2"> <p> 시작 시간과 장 제목 사이의 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 10픽셀의 회색 버다나 글꼴을 사용하여 장 시작 시간을 설정하고 오른쪽에 10픽셀 패딩이 있습니다.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

비디오 장 제목은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**비디오 장 제목의 CSS 속성**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 텍스트 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 글꼴 모음. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 10픽셀의 Verdana 글꼴을 사용하는 비디오 장 제목을 설정하려면

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

비디오 장 설명은 다음과 같은 CSS 클래스 선택기에 의해 제어됩니다.

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

**비디오 장 설명 CSS 속성**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 텍스트 색상 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 글꼴 모음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 선 높이  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 줄 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 내부 패딩입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 연한 회색 배경의 11픽셀 버다나 글꼴로 비디오 장 설명을 설정하려면5픽셀 선 높이, 12픽셀 가로 패딩, 12픽셀 위쪽 패딩 및 9픽셀 아래쪽 패딩.

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

장 버블 아래쪽에 있는 웨지 커넥터는 다음과 같은 CSS 클래스 선택기에 의해 제어됩니다.

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**웨지 커넥터의 CSS 속성**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color  </span> </p> </td> 
   <td colname="col2"> <p>웨지 커넥터 색상. </p> <p>위쪽 테두리 색상만 정의되고 나머지 테두리가 투명하게 표시되도록 <span class="codeph"> &lt;color&gt; 투명 </span>으로 정의됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 폭  </span> </p> </td> 
   <td colname="col2"> <p> 웨지 커넥터 너비. </p> <p>위쪽 및 가로 경계에만 동일한 너비가 정의되고 아래쪽 테두리 너비는 <span class="codeph"> 0 </span>이 되도록 <span class="codeph"> &lt;width&gt; </span>로 정의됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 음수 아래쪽 여백만 정의합니다. 이 값은 <span class="codeph"> border-width </span>의 값과 같아야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 회색 6픽셀 웨지 커넥터를 설정하려면

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

