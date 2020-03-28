---
description: 뷰어는 AEM Assets의 다이내믹 미디어에서 원래 핫스팟이 작성되었던 위치의 기본 보기 위에 핫스팟 아이콘을 표시합니다.
seo-description: 뷰어는 AEM Assets의 다이내믹 미디어에서 원래 핫스팟이 작성되었던 위치의 기본 보기 위에 핫스팟 아이콘을 표시합니다.
seo-title: 핫스팟 및 이미지 맵
solution: Experience Manager
title: 핫스팟 및 이미지 맵
topic: Dynamic media
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 핫스팟 및 이미지 맵{#hotspots-and-image-maps}

뷰어는 AEM Assets의 다이내믹 미디어에서 원래 핫스팟이 작성되었던 위치의 기본 보기 위에 핫스팟 아이콘을 표시합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

핫스팟 아이콘의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7carouselviewer .s7imagemapeffect .s7icon
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>핫스팟 아이콘 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>핫스팟 아이콘 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>핫스팟 아이콘 높이. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 서로 다른 두 아이콘 상태에 대해 서로 다른 이미지를 표시하는 56 x 56픽셀 핫스팟 아이콘을 설정합니다.

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**이미지 맵 영역의 CSS 속성**

이미지 맵 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 </span> </p> </td> 
   <td colname="col2"> <p>이미지 맵 영역 채우기 색상 </p> <p>#RGGBB, <span class="codeph"> RGB(R,G,B) </span>또는 <span class="codeph"> RGBA(R,G,B,A) </span><span class="codeph"> </span> 포맷으로 이 색상을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>이미지 맵 영역 채우기 색상 </p> <p>#RGGBB, <span class="codeph"> RGB(R,G,B) </span>또는 <span class="codeph"> RGBA(R,G,B,A) </span><span class="codeph"> </span> 포맷으로 이 색상을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p> 이미지 맵 영역 테두리 스타일입니다. "폭 <span class="codeph"> "으로 지정해야 합니다. 여기서 </span> 색상이 표현되는 색상은 #RRBB, RGB(R, G, B), RGBA 또는 RGBA(R, G, B, A)로 설정되어 <span class="codeph"> 있고 </span><span class="codeph"> </span> <span class="codeph"> </span> <span class="codeph"> </span><span class="codeph"> </span><span class="codeph"> </span>색상은 #RBB, RGB(R, G B, A)로 설정됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 단일 픽셀 검정 테두리로 투명한 이미지 맵 영역을 설정합니다.

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

