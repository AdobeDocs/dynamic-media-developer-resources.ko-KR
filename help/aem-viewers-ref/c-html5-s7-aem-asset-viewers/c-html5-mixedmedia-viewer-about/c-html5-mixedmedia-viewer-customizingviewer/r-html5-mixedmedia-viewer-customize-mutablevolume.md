---
title: 가변 볼륨
description: 가변 볼륨 컨트롤은 처음에 사용자가 비디오 플레이어 사운드를 음소거하거나 음소거를 해제할 수 있는 단추로 나타납니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 9afa56f9-443c-4307-843c-d7ddba6ec604
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# 가변 볼륨{#mutable-volume}

가변 볼륨 컨트롤은 처음에 사용자가 비디오 플레이어 사운드를 음소거하거나 음소거를 해제할 수 있는 단추로 나타납니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

사용자가 버튼을 롤오버하면 사용자가 볼륨을 설정할 수 있는 슬라이더가 나타납니다. 가변 볼륨 컨트롤은 CSS별로 크기를 지정하고, 스킨을 지정하고, 해당 컨트롤을 포함하는 컨트롤 막대를 기준으로 위치를 지정할 수 있습니다.

가변 볼륨 영역의 모양은 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```
.s7mixedmediaviewer .s7mutablevolume
```

**변경 가능한 볼륨의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 위쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p> 패딩을 포함하여 오른쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 가변 볼륨 컨트롤의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>가변 볼륨 컨트롤의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 변경 가능한 볼륨 컨트롤의 색상입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

음소거/음소거 해제 단추 모양은 다음 CSS 클래스 선택기를 사용하여 제어합니다.

```
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton
```

각 단추 상태에 대한 배경 이미지를 제어할 수 있습니다. 단추의 크기는 볼륨 컨트롤의 크기에서 상속됩니다.

**단추 이미지의 CSS 속성**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 지정된 버튼 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 및 `selected` 특성 선택기를 모두 지원합니다. 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히 `selected='true'`은(는) &quot;음소거&quot; 상태에 해당하며 `selected='false'`은(는) &quot;음소거 해제&quot; 상태에 해당합니다.

세로 볼륨 막대 영역은 다음 CSS 클래스 선택기로 제어합니다.

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume
```

**세로 볼륨 막대 영역의 CSS 속성**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

수직 볼륨 컨트롤 내부의 트랙은 다음 CSS 클래스 선택기를 사용하여 제어됩니다.

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**수직 볼륨 컨트롤의 CSS 속성**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨 컨트롤의 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 컨트롤의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

수직 볼륨 노브는 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7knob
```

세로 볼륨 컨트롤 노브의 **CSS 속성**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 세로 볼륨 조절 손잡이 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS 스프라이트 </a>을(를) 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 조절 손잡이의 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 조절 손잡이의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 남음 </span> </p> </td> 
   <td colname="col2"> <p>세로 볼륨 조절 손잡이의 가로 위치. </p> </td> 
  </tr> 
 </tbody> 
</table>

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)를 참조하십시오.

## 예제 {#section-e8caea0a303c425a8a637c2a47c06355}

위쪽에서 6픽셀, 컨트롤 막대의 오른쪽 가장자리에서 38픽셀로 32x32픽셀 음소거 단추를 설정합니다. 선택하거나 선택하지 않을 때 4개의 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시합니다.

```
.s7mixedmediaviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7mixedmediaviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

다음은 가변 볼륨 컨트롤 내에서 볼륨 슬라이더를 스타일링하는 방법의 예입니다.

```
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7mixedmediaviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```
