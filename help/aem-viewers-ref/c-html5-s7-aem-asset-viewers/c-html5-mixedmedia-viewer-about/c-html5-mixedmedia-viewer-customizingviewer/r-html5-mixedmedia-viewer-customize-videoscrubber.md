---
title: 비디오 스크러버
description: 비디오 스크러버는 사용자가 현재 재생 중인 비디오 내의 모든 시간 위치를 동적으로 찾을 수 있는 가로 슬라이더 컨트롤입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3e9c8800-fda2-41d1-8436-b2de7952652c
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 3%

---

# 비디오 스크러버{#video-scrubber}

비디오 스크러버는 사용자가 현재 재생 중인 비디오 내의 모든 시간 위치를 동적으로 찾을 수 있는 가로 슬라이더 컨트롤입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

비디오가 재생될 때 스크러버 &#39;손잡이&#39;도 움직여서 재생 중 비디오의 현재 시간 위치를 가리킨다. 비디오 스크러버는 항상 컨트롤 막대의 전체 너비를 사용합니다. CSS를 사용하여 비디오 스크러버의 스킨을 만들고, 높이 및 세로 위치를 변경할 수 있습니다.

비디오 스크러버의 일반적인 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7videoscrubber 
.s7mixedmediaviewer .s7videoscrubber .s7videotime 
.s7mixedmediaviewer .s7videoscrubber .s7knob
```

**비디오 스크러버의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 위쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 아래쪽 테두리에서 위치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버 색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 배경, 재생 및 로드 지표를 추적합니다.

```
.s7mixedmediaviewer .s7videoscrubber .s7track 
.s7mixedmediaviewer .s7videoscrubber .s7trackloaded 
.s7mixedmediaviewer .s7videoscrubber .s7trackplayed
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
   <td colname="col2"> <p>해당 트랙의 색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 손잡이를 제어합니다.

```
.s7mixedmediaviewer .s7videoscrubber .s7knob
```

**노브의 CSS 속성**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>세로 손잡이 오프셋. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>손잡이 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>손잡이 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>손잡이 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS 스프라이트 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 CSS 클래스 선택기는 재생된 시간 버블을 제어합니다.

```
.s7mixedmediaviewer .s7videoscrubber .s7videotime
```

**재생된 시간의 CSS 속성 버블**

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
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 시간 표시 텍스트에 사용할 글꼴 색상입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>거품 영역 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>버블 영역 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>버블 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>다음을 참조하십시오 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS 스프라이트 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>텍스트를 버블 영역과 정렬합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

비디오 스크러버 도구 팁을 현지화할 수 있습니다. 다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) 추가 정보.

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

사용자 지정 트랙 색상이 10픽셀 높이이고 컨트롤 막대의 위쪽 및 왼쪽 가장자리에서 10픽셀 및 35픽셀로 배치된 비디오 스크러버와 함께 혼합 미디어 뷰어를 설정합니다.

```
.s7mixedmediaviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```
