---
title: 조치 수행 질문
description: 비디오가 종료되고 특정 비디오와 연결된 모든 대화형 색상 견본을 표시할 때 [액션 호출] 패널이 나타납니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 43e0ffb3-d650-4b79-ab48-2f32b313b832
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 2%

---

# 조치 수행 질문{#call-to-action}

비디오가 종료되고 특정 비디오와 연결된 모든 대화형 색상 견본을 표시할 때 [액션 호출] 패널이 나타납니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

패널은 비디오 제목을 표시하는 헤더 영역, 오른쪽 위 모서리의 재생 단추, 스크롤 가능한 그리드로 표시되는 실제 대화형 색상 견본으로 구성됩니다. [callToActionRemap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6) 구성 속성을 사용하여 패널을 비활성화할 수 있습니다.

작업 패널에 대한 호출은 항상 사용 가능한 전체 뷰어 영역을 사용합니다.

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

다음 CSS 클래스 선택기는 작업 패널 호출에서 배경색의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction
```

## 작업 패널 호출 배경색의 CSS 속성 {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p> 작업 패널 호출 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example}

어두운 회색 배경을 사용하여 작업 패널에 대한 호출을 설정하려면 다음을 수행하십시오.

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

다음 CSS 클래스 선택기는 작업 패널 호출에서 헤더의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## 작업 패널 헤더에 대한 호출의 CSS 속성 {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>헤더의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>헤더의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 하단  </span> </p> </td> 
   <td colname="col2"> <p>헤더의 아래쪽 테두리. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example-1}

70픽셀이고, 어두운 회색 배경이 있고, 하단을 따라 약간 더 밝은 회색의 2픽셀 테두리가 있는 헤더를 설정하려면 다음을 수행하십시오.

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

다음 CSS 클래스 선택기는 작업 패널 호출에서 헤더 제목의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## 작업 패널 호출에 있는 헤더 제목의 CSS 속성:  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 배너 내의 텍스트 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 라인 높이  </span> </p> </td> 
   <td colname="col2"> <p>선 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> 글꼴 패밀리. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>배너의 텍스트 정렬. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 패딩  </span> </p> </td> 
   <td colname="col2"> <p>왼쪽 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 패딩  </span> </p> </td> 
   <td colname="col2"> <p> 재생 단추에 사용할 공간을 허용하는 오른쪽 패딩. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example-2}

70픽셀 선 높이, 25픽셀 글꼴 크기, 흰색 색상 및 왼쪽 정렬로 비디오 제목을 설정하려면 다음을 수행하십시오.

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

다음 CSS 클래스 선택기는 작업 호출 패널에서 닫기 버튼의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## 작업 패널 호출에 있는 닫기 버튼의 CSS 속성: {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 헤더 상단에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 헤더의 오른쪽에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>단추 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p> 단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p>CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하며, 이 선택기를 사용하여 다른 스킨을 다른 단추 상태에 적용할 수 있습니다.

## 예 {#example-3}

28 x 28픽셀인 재생 단추를 설정하려면 다음을 수행하십시오. 버튼은 헤더의 위쪽 및 오른쪽 가장자리로부터 20픽셀을 배치해야 합니다. 또한, 서로 다른 네 가지 단추 상태 각각에 대해 다른 이미지를 표시해야 합니다. 구성 요소의 스프라이트 이미지에서 아트웍을 가져옵니다.

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

다음 CSS 클래스 선택기는 작업 패널에 대한 호출에서 축소판 표 보기의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## 작업 패널 호출에서 축소판 표 보기의 CSS 속성:  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>축소판 영역의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example-4}

어두운 회색 배경을 사용하여 축소판 영역을 설정하려면 다음을 수행하십시오.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

다음 CSS 클래스 선택기는 [액션 호출] 패널에서 thumb 셀의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## 동작 패널에 있는 축소판 셀의 CSS 속성: {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 각 축소판 주위의 가로 및 세로 여백의 크기입니다. </p> <p>실제 가로 축소판 간격은 <span class="codeph"> .s7thumbcell </span>에 대해 설정된 왼쪽 및 오른쪽 여백 집합의 합계와 같습니다. 세로 간격에도 동일한 규칙이 적용됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example-5}

24픽셀의 가로 간격과 18픽셀의 세로 간격을 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

다음 CSS 클래스 선택기는 작업 패널 호출에서 축소판의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## 작업 패널 호출 축소판의 CSS 속성: {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>축소판의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p>축소판의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p>축소판의 테두리입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>섬네일은 `state` 속성 선택기를 지원합니다. 이 선택기는 다른 스킨(thumbnail states)을 적용하는 데 사용할 수 있습니다. 특히 `state="selected"` 은 현재 선택한 이미지의 축소판에 해당합니다. `state="default"`은 나머지 축소판에 해당합니다. 마우스 가리키기에 `state="over"`가 사용됩니다.

## 예 {#example-6}

94 x 100픽셀인 축소판을 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

다음 CSS 클래스 선택기는 작업 패널 호출에서 축소판 레이블의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## 작업 패널 호출에 있는 축소판 레이블의 CSS 속성: {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색상  </span> </p> </td> 
   <td colname="col2"> <p> 레이블의 텍스트 색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>레이블의 가로 정렬. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>글꼴 패밀리. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example-7}

흰색 색상을 사용하는 레이블을 설정하려면 가운데 맞춤을 15픽셀로 하고 Arial® 글꼴을 사용합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

보기에 세로로 맞출 수 있는 것보다 더 많은 축소판이 있는 경우 축소판은 오른쪽의 세로 스크롤 막대를 렌더링합니다. 기본적으로 [액션] 패널에 대한 호출은 엄지와 스크롤 단추 없이 작은 세로 막대를 렌더링합니다. 그러나 뷰어 CSS를 변경하여 막대를 사용자 지정할 수 있습니다.

다음 CSS 클래스 선택기는 작업 패널 호출에서 스크롤 막대 영역의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## 동작 패널 호출에서 스크롤 막대 영역의 CSS 속성: {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p> 스크롤 막대의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>축소판 영역의 맨 위에서 수직 스크롤 막대 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>축소판 영역의 아래쪽에서 수직 스크롤 막대 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 축소판 영역의 오른쪽 모서리에서 가로 스크롤바가 오프셋됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example-8}

축소판 영역의 위쪽, 오른쪽 또는 아래쪽의 여백이 없는 22픽셀인 스크롤 막대를 설정하려면 다음을 수행하십시오.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

스크롤 막대 트랙은 위쪽 및 아래쪽 스크롤 막대 단추 사이의 영역입니다. 구성 요소는 트랙의 위치와 높이를 자동으로 설정합니다.

다음 CSS 클래스 선택기는 작업 호출 패널에서 스크롤 막대 트랙의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## 스크롤 추적 막대의 CSS 속성 {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>스크롤 트랙 막대의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>트랙 막대의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example-9}

가로 22픽셀이고 회색 색상을 갖는 스크롤 막대 트랙을 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

스크롤 막대 엄지는 스크롤 트랙 영역 내에서 세로로 이동합니다. 세로 위치는 구성 요소 논리에 의해 완전히 제어됩니다. 그러나 엄지 높이 는 콘텐츠의 양에 따라 동적으로 변경되지 않습니다.

다음 CSS 클래스 선택기는 엄지 높이 및 기타 종횡비의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## 동작 패널 호출에서 축소판 높이의 CSS 속성: {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>엄지 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p>엄지 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 탑  </span> </p> </td> 
   <td colname="col2"> <p>트랙 위쪽 사이의 수직 안쪽 여백입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 하단  </span> </p> </td> 
   <td colname="col2"> <p>트랙 아래쪽 사이의 수직 안쪽 여백을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 테두리 반경  </span> </p> </td> 
   <td colname="col2"> <p>테두리의 반경. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>엄지 색. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p> 주어진 엄지 영역 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb은 `state` 속성 선택기를 지원합니다. 이 선택기는 다음과 같은 다른 thumb 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. `"up"`, `"down"`, `"over"` 및 `"disabled"`.

## 예 {#example-10}

6 x 167 픽셀인 스크롤 막대 엄지를 설정하려면 세 픽셀 라운드 모서리와 회색 색상을 사용합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

다음 CSS 클래스 선택기는 위쪽 및 아래쪽 스크롤 단추의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

CSS 위쪽, 왼쪽, 아래쪽 또는 오른쪽 속성을 사용하여 스크롤 단추를 배치할 수 없습니다. 뷰어 논리는 자동으로 위치를 지정합니다. 대화형 비디오 뷰어의 작업 패널에 대한 호출은 스크롤 막대에서 이러한 단추를 사용하지 않으므로 기본 CSS에서 해당 크기가 0픽셀로 설정됩니다.

## 동작 패널 호출에서 위쪽 및 아래쪽 스크롤 단추의 CSS 속성:  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p> 단추 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p>단추 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이러한 버튼은 `state` 속성 선택기를 지원하며, 이 선택기를 사용하여 다음과 같은 다른 thumb 상태에 다른 스킨을 적용할 수 있습니다. `"up"`, `"down"`, `"over"` 및 `"disabled"`.

단추 도구 설명은 현지화할 수 있습니다. [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)을 참조하십시오.

## 예 {#example-11}

스크롤 단추의 크기를 0으로 설정하고 이를 숨겨서 스크롤 단추를 비활성화합니다.

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```
