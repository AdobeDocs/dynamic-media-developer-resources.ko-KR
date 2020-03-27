---
description: 비디오 scrubber는 사용자가 현재 재생 중인 비디오 내에서 임의의 시간 위치를 동적으로 검색할 수 있도록 해주는 수평 슬라이더 컨트롤입니다.
seo-description: 비디오 scrubber는 사용자가 현재 재생 중인 비디오 내에서 임의의 시간 위치를 동적으로 검색할 수 있도록 해주는 수평 슬라이더 컨트롤입니다.
seo-title: 비디오 스크러버
solution: Experience Manager
title: 비디오 스크러버
topic: Dynamic media
uuid: cfd1055b-c4d6-42e4-ad24-a897e923e8e9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video scrubber{#video-scrubber}

비디오 scrubber는 사용자가 현재 재생 중인 비디오 내에서 임의의 시간 위치를 동적으로 검색할 수 있도록 해주는 수평 슬라이더 컨트롤입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

또한 scrubber는 비디오가 재생되는 동안 비디오의 현재 위치를 나타내기 위해 재생될 때 이동합니다. 비디오 스크러버는 항상 컨트롤 막대의 전체 너비를 사용합니다. 비디오 스크러버를 피울 수 있다. 높이와 세로 위치를 CSS로 변경합니다.

비디오 scrubber의 일반적인 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber 
.s7interactivevideoviewer .s7videoscrubber .s7videotime 
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**비디오 스크러버 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 아래쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버 색상입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 배경, 재생 및 로드 표시기를 추적합니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7track 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed
```

**트랙의 CSS 속성**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>해당 트랙의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>해당 트랙의 색상입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 노브를 제어합니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**노브의 CSS 속성**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>수직 노브 오프셋. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>노브 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>손잡이의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>아트웍을 조절합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 재생되는 버블 시간을 제어합니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7videotime
```

**재생된 시간 버블의 CSS 속성**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 모음입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기 </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>아트웍을 버블링합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>버블 영역과 텍스트 정렬 </p> </td> 
  </tr> 
 </tbody> 
</table>

비디오 스크러버 도구 설명을 현지화할 수 있습니다. 자세한 [내용은 사용자 인터페이스 요소의](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 현지화를 참조하십시오.

**예** - 10픽셀의 사용자 정의 트랙 색상이 있는 비디오 스크러버를 설정하고 컨트롤 막대의 상단 및 왼쪽 가장자리에서 10픽셀과 35픽셀을 배치하려면

```
.s7interactivevideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

매개 변수를 사용하여 비디오 장(chapter) 작업이 활성화되면 장 위치가 비디오 스크러버 트랙 위쪽에 마커로 표시됩니다. `navigation`

비디오 장 마커는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation
```

**비디오 장 마커의 CSS 속성**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 마커 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 마커 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 마커 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 속성 선택기를 지원합니다. 이 선택기를 사용하면 다른 단추 상태에 다른 스킨을 적용할 수 있습니다. 특히, `selected='default'` 기본 비디오 장 마커 상태에 해당하며, 마우스 위나 터치 제스처로 비디오 장 마커를 활성화할 `selected='over'` 때 사용됩니다.

**예** - 5 x 8픽셀의 비디오 장 마커를 설정하고 &quot;기본값&quot; 및 &quot;오버&quot; 상태에 다른 아트를 사용하려면

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

비디오 장(chapter) 버블은 비디오 장 마커 위쪽에 배치되고 지정된 장의 제목, 시작 시간 및 설명을 표시합니다. 비디오 scrubber 트랙을 기준으로 버블 너비와 수직 오프셋을 최대 크기로 제어할 수 있습니다. 나머지 항목은 구성 요소에 의해 자동으로 계산됩니다.

비디오 장 버블은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter
```

**비디오 장 버블의 CSS 속성**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블의 최대 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버 트랙의 수직 오프셋입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 비디오 스크러버 트랙의 아래쪽에서 235픽셀이고 8픽셀인 비디오 장 버블을 설정하려면

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

비디오 장 버블은 선택적인 헤더와 컨텐츠로 구성됩니다. 헤더에는 장 시작 시간과 장 제목이 선택 사항입니다.

헤더는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header
```

**비디오 장 버블 헤더의 CSS 속성**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 헤더 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 머리글 텍스트의 내부 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 헤더 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 선 높이 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 헤더 텍스트 줄 높이. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 22픽셀 높이, 22픽셀 선 높이, 12픽셀 가로 여백 및 회색 배경인 비디오 장 버블 헤더를 설정하려면

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

비디오 장의 시작 시간은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**비디오 장 시작 시간의 CSS 속성**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께 </span> </p> </td> 
   <td colname="col2"> <p>글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기 </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 모음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 시작 시간과 장 제목 사이의 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 회색 Verdana 글꼴을 사용하여 장 시작 시간을 설정하려면 오른쪽에 10픽셀 패딩이 있어야 합니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

비디오 장 제목은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**비디오 장 제목의 CSS 속성**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 글꼴 모음. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 10픽셀의 Verdana 글꼴을 사용하는 비디오 장 제목을 설정하려면

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

비디오 장 설명은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description
```

**비디오 장 설명의 CSS 속성**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 두께 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 글꼴 크기 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 글꼴 크기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 글꼴 모음. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 선 높이 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 줄 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 연한 회색 배경과 함께 11픽셀의 Verdana 글꼴을 사용하여 비디오 장 설명을 설정하려면5픽셀 선 높이, 12픽셀 가로 패딩, 12픽셀 위쪽 패딩 및 9픽셀 아래쪽 패딩.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

장 버블 아래쪽에 있는 웨지 커넥터는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail
```

**웨지 커넥터의 CSS 속성**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 색상 </span> </p> </td> 
   <td colname="col2"> <p>웨지 커넥터 색상 </p> <p>위쪽 테두리 색상만 정의되고 나머지 테두리가 투명하게 표시되도록 <span class="codeph"> &lt;color&gt; 투명 투명으로 </span> 정의됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 너비 </span> </p> </td> 
   <td colname="col2"> <p> 웨지 커넥터 너비. </p> <p>위쪽 및 가로 경계에만 동일한 너비가 정의되고 아래쪽 테두리 너비는 <span class="codeph"> 0이 되도록 &lt;width&gt; &lt;width&gt; 0으로 </span> 정의됩니다 <span class="codeph"> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 음수 아래쪽 여백만 정의합니다. 테두리 <span class="codeph"> 너비와 동일한 값을 가져야 합니다 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예** - 회색 6픽셀 웨지 커넥터를 설정하려면

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

