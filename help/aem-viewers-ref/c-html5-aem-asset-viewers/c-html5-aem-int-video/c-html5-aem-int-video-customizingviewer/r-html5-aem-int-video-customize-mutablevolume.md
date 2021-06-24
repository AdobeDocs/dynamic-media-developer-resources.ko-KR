---
description: 가변 볼륨 컨트롤은 처음에 사용자가 비디오 플레이어 사운드를 음소거하거나 음소거할 수 있는 단추로 나타납니다.
solution: Experience Manager
title: 가변 볼륨
feature: Dynamic Media Classic,Viewers,SDK/API,대화형 비디오
role: Developer,Business Practitioner
exl-id: ecef47c1-e659-4930-bfb1-cc5e7c059094
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 2%

---

# 가변 볼륨{#mutable-volume}

가변 볼륨 컨트롤은 처음에 사용자가 비디오 플레이어 사운드를 음소거하거나 음소거할 수 있는 단추로 나타납니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

사용자가 단추를 롤오버하면 사용자가 볼륨을 설정할 수 있는 슬라이더가 나타납니다. 가변 볼륨 컨트롤은 CSS로 포함되어 있는 컨트롤 막대에 대해 크기 조정, skin 및 배치할 수 있습니다.

가변 볼륨 영역의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7mutablevolume
```

**가변 볼륨의 CSS 속성**

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 가변 볼륨 컨트롤의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>가변 볼륨 컨트롤의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p> 가변 볼륨 컨트롤의 색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

음소거/음소거 해제 단추 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton
```

각 단추 상태에 대한 배경 이미지를 제어할 수 있습니다. 단추의 크기는 볼륨 컨트롤의 크기에서 상속됩니다.

**단추 이미지의 CSS 속성**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 및 `selected` 속성 선택기를 모두 지원하며, 이 선택기는 다른 스킨(skin)을 다른 단추 상태에 적용하는 데 사용할 수 있습니다. 특히 `selected='true'`은 &quot;음소거&quot; 상태에 해당하고 `selected='false'`는 &quot;음소거 해제&quot; 상태에 해당합니다.

세로 볼륨 막대 영역은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume
```

**세로 볼륨 막대 영역의 CSS 속성**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

수직 볼륨 컨트롤 내의 트랙은 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**세로 볼륨 컨트롤 내의 트랙의 CSS 속성**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨 컨트롤의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤의 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

세로 볼륨 노브는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**세로 볼륨 컨트롤 노브의 CSS 속성**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p> 수직 볼륨 컨트롤 노브 아트웍입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비  </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤 노브의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이  </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤 노브의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>수직 볼륨 컨트롤 노브의 수평 위치입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

단추 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

## 예제 {#section-e8caea0a303c425a8a637c2a47c06355}

32 x 32픽셀이고 상단에서 6픽셀이고 컨트롤 막대의 오른쪽 가장자리에서 38픽셀인 음소거 단추를 설정하려면 다음을 수행합니다. 선택하거나 선택하지 않은 경우 4개의 서로 다른 버튼 상태에 대해 다른 이미지를 표시합니다.

```
.s7interactivevideoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

다음은 가변 볼륨 컨트롤 내에서 볼륨 슬라이더의 스타일을 지정하는 방법의 예입니다.

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```
