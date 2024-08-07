---
title: 대화형 견본
description: 대화형 데이터가 구성에서 뷰어에 전달된 경우 비디오 콘텐츠 옆에 대화형 견본 패널이 표시됩니다. 맨 위에 "클릭하여 보기" 등의 텍스트를 렌더링하는 배너, 하나 이상의 대화형 견본 열 및 두 개의 스크롤 단추(데스크탑 시스템에서만 사용 가능)로 구성됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# 대화형 견본{#interactive-swatches}

대화형 데이터가 구성에서 뷰어에 전달된 경우 비디오 콘텐츠 옆에 대화형 견본 패널이 표시됩니다. 맨 위에 &quot;클릭하여 보기&quot; 등의 텍스트를 렌더링하는 배너, 하나 이상의 대화형 견본 열 및 두 개의 스크롤 단추(데스크탑 시스템에서만 사용 가능)로 구성됩니다.

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

데스크탑 시스템과 터치 디바이스에서 가로 방향으로 대화형 견본이 비디오 컨텐츠의 오른쪽에 세로로 렌더링됩니다. 터치 장치에서 세로 방향으로 표시된다면 뷰어 하단에 가로 색상 견본 행으로 표시됩니다.

다음 CSS 클래스 선택기는 대화형 견본 패널의 위치 및 방향을 제어합니다.

```
.s7interactivevideoviewer .s7interactiveswatches
```

## 대화형 견본의 CSS 속성 {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>대화형 견본 패널의 폭 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>대화형 견본 패널의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p>대화형 견본 패널의 위쪽 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>대화형 견본 패널의 하단 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 남음 </span> </p> </td> 
   <td colname="col2"> <p>대화형 견본 패널의 왼쪽 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>대화형 견본 패널의 오른쪽 위치입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

대화형 견본 패널의 런타임 위치 및 방향은 다음과 같이 위의 CSS 속성의 조합으로 정의됩니다.

* 뷰어 하단에 대화형 견본을 가로로 렌더링하려면 높이를 절대 픽셀 값으로, 왼쪽 및 아래를 0px로, 너비, 오른쪽 및 위쪽을 auto로 설정합니다.
* 대화형 견본을 비디오 컨텐츠의 오른쪽에 세로로 렌더링하려면 너비를 절대 픽셀로, 오른쪽과 위쪽을 0픽셀로, 높이, 왼쪽 및 아래쪽을 auto로 설정합니다.

이 스타일에 CSS 마커를 사용하여 대화형 색상 견본 패널의 적응형 배치를 수행할 수 있습니다.

## 예 {#example}

터치 디바이스에서 가로 방향으로 뷰어 하단에 가로로 렌더링하도록 대화형 견본 패널을 설정하려면. 또한 다른 모든 경우에 비디오 컨텐츠의 오른쪽에 세로로 표시하려면 다음을 수행하십시오.

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

배너의 크기 및 위치는 CSS를 사용하여 적용된 다른 스타일을 기반으로 대화형 견본 구성 요소에서 관리하며 명시적으로 설정할 수 없습니다.

다음 CSS 클래스 선택기는 배너 패널의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## 배너 패널의 CSS 속성 {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>배너 패널의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p>배너 패널 내의 텍스트 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 </span> </p> </td> 
   <td colname="col2"> <p>배너 패널 주변의 테두리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>배너 패널 내의 텍스트에 사용할 글꼴 두께입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>배너 패널 내의 텍스트에 사용할 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>배너 패널 내의 텍스트에 사용할 글꼴 모음 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>배너 패널 내의 텍스트에 사용할 글꼴 맞춤입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

배너 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

어두운 회색 배경과 밝은 회색 2픽셀 테두리 및 흰색 텍스트가 가로 가운데에 있는 배너를 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

다음 CSS 클래스 선택기는 색상 견본의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## 견본 영역의 CSS 속성 {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>견본 영역의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-9cadd62a09fd44a280f55ff42437e416}

어두운 회색 배경의 색상 견본 영역을 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

다음 CSS 클래스 선택기는 견본 썸네일 간의 간격을 제어합니다.

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## 견본 썸네일 간격의 CSS 속성 {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 </span> </p> </td> 
   <td colname="col2"> <p> 각 썸네일 주변의 가로 및 세로 여백 크기입니다. 실제 썸네일 간격은 <span class="codeph"> .s7thumbcell </span>에 설정된 왼쪽 및 오른쪽 여백의 합계와 같습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-39fb270b7e494a9d99e6e8f6890ec53c}

세로 간격을 10픽셀로 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

다음 CSS 클래스 선택기는 개별 썸네일의 모양을 제어합니다.

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## 개별 썸네일 모양의 CSS 속성 {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 </span> </p> </td> 
   <td colname="col2"> <p>썸네일의 테두리. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>썸네일은 `state` 특성 선택기를 지원하며, 이 선택기를 사용하여 다른 썸네일 상태에 다른 스킨을 적용할 수 있습니다. 특히 `state="selected"`은(는) 현재 선택한 이미지의 썸네일에 해당합니다. `state="default"`은(는) 나머지 썸네일에 해당합니다. `state="over"`은(는) 마우스 가리키기에 사용됩니다.

## 예 {#section-69fec189ffaa440b97b6b846c320b75b}

100 x 75픽셀의 썸네일을 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

다음 CSS 클래스 선택기는 썸네일 레이블의 모양을 제어합니다.

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## 썸네일 레이블 모양의 CSS 속성 {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
   <td colname="col2"> <p>텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 </span> </p> </td> 
   <td colname="col2"> <p>레이블 테두리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 텍스트 맞춤 </span> </p> </td> 
   <td colname="col2"> <p>가로 텍스트 정렬. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-eb141eb6c1154183baa69796edb90536}

왼쪽 맞춤, 흰색, 12픽셀, Helvetica® 글꼴 및 아래쪽 테두리를 사용하도록 레이블을 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

다음 CSS 클래스 선택기는 위쪽 및 아래쪽 스크롤 단추의 모양을 제어합니다.

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

CSS `top`, `left`, `bottom` 및 `right` 속성을 사용하여 스크롤 단추를 배치할 수 없습니다. 대신 뷰어 논리에서 자동으로 배치합니다.

## 위쪽 및 아래쪽 스크롤 단추 모양에 대한 CSS 속성 {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>스크롤 단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p>CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부의 위치입니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 특성 선택기를 지원하며, 이 선택기를 사용하여 단추 상태에 다른 스킨을 적용할 수 있습니다. &quot; `up`&quot;, &quot; `down`&quot;, &quot; `over`&quot; 및 &quot; `disabled`&quot;.

버튼 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

## 예 {#section-e6ce4fa084b84288bc7583342b2c510c}

60 x 36픽셀인 위로 스크롤 단추를 설정하려면 각 상태에 대해 다른 아트웍을 사용하고 구성 요소의 스프라이트 이미지에서 해당 아트웍을 가져옵니다.

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```
