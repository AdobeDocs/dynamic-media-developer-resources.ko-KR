---
description: 변경 가능한 볼륨 컨트롤은 처음에 사용자가 비디오 플레이어 사운드의 음소거 또는 음소거를 해제할 수 있는 단추로 나타납니다.
seo-description: 변경 가능한 볼륨 컨트롤은 처음에 사용자가 비디오 플레이어 사운드의 음소거 또는 음소거를 해제할 수 있는 단추로 나타납니다.
seo-title: 가변 볼륨
solution: Experience Manager
title: 가변 볼륨
topic: Dynamic media
uuid: 3c3239ca-18fc-47ff-bc5d-2b50e1514e50
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Mutable volume{#mutable-volume}

변경 가능한 볼륨 컨트롤은 처음에 사용자가 비디오 플레이어 사운드의 음소거 또는 음소거를 해제할 수 있는 단추로 나타납니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

사용자가 단추 위로 롤오버하면 사용자가 볼륨을 설정할 수 있는 슬라이더가 나타납니다. 가변 볼륨 컨트롤은 CSS를 통해 포함된 컨트롤 막대와 상대적으로 크기 조정, 스킨 및 위치를 지정할 수 있습니다.

가변 볼륨 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col2"> <p> 패딩 등 오른쪽 테두리에서 위치를 지정할 수 있습니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 가변 볼륨 컨트롤의 색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

음소거/음소거 해제 단추 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton
```

각 단추 상태에 대한 배경 이미지를 제어할 수 있습니다. 단추 크기는 볼륨 컨트롤의 크기에서 상속됩니다.

**단추 이미지의 CSS 속성**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 및 `selected` 속성 선택기를 모두 지원합니다. 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히 `selected='true'` &quot;음소거&quot; 상태에 해당하며 &quot;음소거 해제&quot; 상태에 `selected='false'` 해당합니다.

세로 볼륨 막대 영역은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume
```

**세로 볼륨 막대 영역의 CSS 속성**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

세로 볼륨 컨트롤 내의 트랙은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**수직 볼륨 컨트롤 내의 트랙의 CSS 속성**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨 컨트롤의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤의 너비입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

세로 볼륨 노브는 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**세로 볼륨 컨트롤 노브의 CSS 속성**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 수직 볼륨 컨트롤 아트웍을 조절합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤 노브의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤 노브의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤 노브의 가로 위치입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

단추 도구 설명을 현지화할 수 있습니다. 자세한 [내용은 사용자 인터페이스 요소의](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 현지화를 참조하십시오.

## 예제 {#section-e8caea0a303c425a8a637c2a47c06355}

32 x 32픽셀이고 위쪽에서 6픽셀, 컨트롤 막대의 오른쪽 가장자리에서 38픽셀인 음소거 단추를 설정하려면 선택되거나 선택하지 않을 때 4개의 서로 다른 단추 상태에 대해 다른 이미지를 표시합니다.

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

