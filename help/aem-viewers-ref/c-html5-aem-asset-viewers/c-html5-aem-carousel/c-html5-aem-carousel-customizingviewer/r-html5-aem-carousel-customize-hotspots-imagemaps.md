---
title: 핫스팟 및 이미지 맵
description: 뷰어는 원래 AEM Assets의 Dynamic Media에서 핫스팟이 작성된 위치의 기본 보기에 핫스팟 아이콘을 표시합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---

# 핫스팟 및 이미지 맵{#hotspots-and-image-maps}

뷰어는 원래 AEM Assets의 Dynamic Media에서 핫스팟이 작성된 위치의 기본 보기에 핫스팟 아이콘을 표시합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

핫스팟 아이콘의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p>핫스팟 아이콘 아트웍입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p>CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>를 참조하십시오. </p> </td> 
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

예 - 두 개의 서로 다른 아이콘 상태에 대해 서로 다른 이미지를 표시하는 56 x 56 픽셀 핫스팟 아이콘을 설정합니다.

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

이미지 맵 영역의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> 배경  </span> </p> </td> 
   <td colname="col2"> <p>이미지 맵 영역 채우기 색입니다. </p> <p><span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> 또는 <span class="codeph"> RGBA(R,G,B,A) </span> 형식으로 이 색상을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>이미지 맵 영역 채우기 색입니다. </p> <p><span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> 또는 <span class="codeph"> RGBA(R,G,B,A) </span> 형식으로 이 색상을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p> 이미지 맵 영역 테두리 스타일입니다. <span class="codeph"> 너비 </span> <span class="codeph"> 단색 </span>"로 지정해야 합니다. 여기서 <span class="codeph"> 너비 </span>는 픽셀로 표현되고 <span class="codeph"> 색상 </span>은 <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> 또는 <span class="codeph"> RR(R,G,B,A) &lt;A13/&gt; 로 설정됩니다.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 한 픽셀 검정색 테두리로 투명한 이미지 맵 영역을 설정합니다.

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
