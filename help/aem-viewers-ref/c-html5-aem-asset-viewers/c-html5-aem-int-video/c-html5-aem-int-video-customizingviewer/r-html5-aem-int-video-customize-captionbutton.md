---
description: 이 단추는 닫힌 캡션 표시를 설정/해제합니다. caption 매개 변수를 지정하지 않으면 표시되지 않습니다.
solution: Experience Manager
title: 캡션 단추
feature: Dynamic Media Classic,Viewers,SDK/API,대화형 비디오
role: Developer,User
exl-id: 322062a5-1741-45ce-96d7-8710a8246cd6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 2%

---

# 캡션 단추{#caption-button}

이 단추는 닫힌 캡션 표시를 설정/해제합니다. caption 매개 변수를 지정하지 않으면 표시되지 않습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

CSS를 사용하여 이 단추를 포함하는 컨트롤 막대를 기준으로 크기를 지정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.

이 단추의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7closedcaptionbutton
```

**캡션 단추의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 오른쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 왼쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 아래쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 전체 화면 단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>전체 화면 단추의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시된 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 및 `selected` 속성 선택기를 모두 지원하며, 이 선택기는 다른 스킨(skin)을 다른 단추 상태에 적용하는 데 사용할 수 있습니다. 특히 `selected='true'` 은 캡션이 표시될 때 상태에 해당하고 캡션이 숨겨질 때 `selected='false'` 이 사용됩니다.

단추 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

## 예 {#section-e8caea0a303c425a8a637c2a47c06355}

28 x 28픽셀인 닫힌 캡션 단추를 설정하려면 컨트롤 막대의 오른쪽 가장자리로부터 4픽셀, 오른쪽 가장자리에서는 68픽셀을 배치하여 선택 여부에 따라 4개의 서로 다른 단추 상태에 대해 다른 이미지를 표시합니다.

```
.s7interactivevideoviewer .s7closedcaptionbutton { 
 position:absolute; 
 top:4px; 
 right:68px; 
 width:28px; 
 height:28px; 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='true'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_up.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='true'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='true'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='false'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='false'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='false'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7interactivevideoviewer .s7closedcaptionbutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png);  
}
```
