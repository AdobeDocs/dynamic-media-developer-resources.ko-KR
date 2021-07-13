---
description: 비디오 스크러버는 사용자가 현재 재생 중인 비디오 내의 임의의 시간 위치를 동적으로 찾을 수 있도록 해주는 가로 슬라이더 컨트롤입니다.
solution: Experience Manager
title: 비디오 스크러버
feature: Dynamic Media Classic,Viewers,SDK/API,대화형 비디오
role: Developer,User
exl-id: 9d11f2e9-315c-44d8-beb1-530d2b316604
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 2%

---

# 비디오 스크러버{#video-scrubber}

비디오 스크러버는 사용자가 현재 재생 중인 비디오 내의 임의의 시간 위치를 동적으로 찾을 수 있도록 해주는 가로 슬라이더 컨트롤입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

또한 스크러버 &#39;노브&#39;는 비디오가 재생되는 동안 비디오의 현재 시간 위치를 나타내기 위해 재생될 때 이동합니다. 비디오 스크러버는 항상 컨트롤 막대의 전체 너비를 사용합니다. 비디오 스크러버를 피울 수 있다. 높이와 세로 위치를 CSS로 변경합니다.

비디오 스크러버의 일반 모양은 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber 
.s7interactivevideoviewer .s7videoscrubber .s7videotime 
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**비디오 스크러버의 CSS 속성**

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
   <td colname="col2"> <p>비디오 스크러버의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버의 색입니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p>해당 트랙의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>해당 트랙의 색입니다. </p> </td> 
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
   <td colname="col2"> <p>손잡이의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p>손잡이의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p>아트웍을 노브. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 재생되는 시간을 제어합니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7videotime
```

**재생되는 시간의 CSS 속성**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 모음입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p>아트웍의 버블. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>텍스트 맞춤을 버블 영역으로 지정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

비디오 스크러버 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

**예**  - 10픽셀 높이의 사용자 지정 트랙 색상이 있는 비디오 스크러버와 컨트롤 막대의 위쪽 및 왼쪽 가장자리에서 10픽셀 및 35픽셀을 배치하여 비디오 뷰어를 설정하려면 다음을 수행하십시오.

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

`navigation` 매개 변수를 사용하여 비디오 chapter가 활성화되면 장 위치가 비디오 스크러버 트랙 맨 위에 마커로 표시됩니다.

비디오 장 마커는 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation
```

**비디오 장 마커의 CSS 속성**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 마커 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 마커 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 마커 아트웍입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하며, 이 선택기를 사용하여 다른 스킨을 다른 단추 상태에 적용할 수 있습니다. 특히 `selected='default'` 은 기본 비디오 장 마커 상태에 해당하며, 마우스로 가리키거나 터치 제스처로 비디오 장 마커를 활성화하면 `selected='over'` 이 사용됩니다.

**예**  - 5 x 8픽셀인 비디오 장 마커를 설정하고 &quot;기본값&quot; 및 &quot;초과&quot; 상태에 다른 아트를 사용합니다.

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

비디오 장 버블은 비디오 장 마커의 맨 위에 배치되며 주어진 장의 제목, 시작 시간 및 설명을 표시합니다. 비디오 스크러버 트랙에 대해 최대 버블 너비 및 수직 오프셋을 제어할 수 있다. 나머지는 구성 요소에 의해 자동으로 계산됩니다.

비디오 장 버블은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter
```

**비디오 장 버블의 CSS 속성**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최대 너비  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블의 최대 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버 트랙에서 수직 오프셋입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 235픽셀이고 비디오 스크러버 트랙 하단에서 8픽셀인 비디오 장 버블을 설정하려면 다음을 수행하십시오.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

비디오 장 버블은 선택적 헤더와 콘텐츠로 구성됩니다. 헤더에는 선택적 장 시작 시간 및 장 제목이 있습니다.

헤더는 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header
```

**비디오 장 버블 헤더의 CSS 속성**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 헤더 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 헤더 텍스트의 내부 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 헤더 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 라인 높이  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 버블 헤더 텍스트 줄 높이. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 22픽셀 높이의 비디오 장 버블 헤더를 설정하려면 22픽셀 라인 높이, 12픽셀 가로 여백 및 회색 배경을 설정하십시오.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

비디오 장의 시작 시간은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**비디오 장 시작 시간의 CSS 속성**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색상  </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 가중치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 패밀리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 패딩  </span> </p> </td> 
   <td colname="col2"> <p> 시작 시간과 장 제목 사이의 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 회색 세로 10픽셀 버다나 글꼴을 사용하여 장 시작 시간을 설정하고 오른쪽에는 열 픽셀 패딩이 있습니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

비디오 장 제목은 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**비디오 장 제목의 CSS 속성**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색상  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 텍스트 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 글꼴 가중치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 제목 글꼴 패밀리입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 흰색, 굵은 10픽셀 버다나 글꼴을 사용하는 비디오 장 제목을 설정하려면 다음을 수행하십시오.

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
   <td colname="col1"> <p> <span class="codeph"> 색상  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 텍스트 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 글꼴 가중치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 글꼴 패밀리입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 라인 높이  </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 줄 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>비디오 장 설명 내부 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 어두운 회색의 11픽셀 버다나 글꼴과 밝은 회색 배경을 사용하여 비디오 장 설명을 설정하려면 다음을 수행하십시오. 5픽셀 라인 높이, 12픽셀 수평 패딩, 12픽셀 위쪽 패딩 및 9픽셀 아래쪽 패딩.

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

장 버블의 맨 아래에 있는 웨지 커넥터는 다음 CSS 클래스 선택기에 의해 제어됩니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail
```

**웨지 커넥터의 CSS 속성**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 색상  </span> </p> </td> 
   <td colname="col2"> <p>웨지 커넥터 색상. </p> <p><span class="codeph"> &lt;color&gt; 투명한 </span>으로 정의되므로 위쪽 테두리 색상만 정의되어 나머지 테두리는 투명하게 유지됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 폭  </span> </p> </td> 
   <td colname="col2"> <p> 웨지 커넥터 너비. </p> <p><span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span>로 정의되므로 위쪽 및 가로 테두리에만 동일한 너비가 정의되고 아래쪽 테두리 너비는 <span class="codeph"> 0 </span>입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 음수 아래쪽 여백만 정의합니다. <span class="codeph"> border-width </span> 값과 동일한 값이 있어야 합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

**예**  - 회색의 6개 픽셀 웨지 커넥터를 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
