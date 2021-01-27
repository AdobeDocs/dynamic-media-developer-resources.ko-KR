---
description: 확대/축소 표시기가 확대/축소 보기 영역에 오버레이됩니다. 이미지가 재설정 상태일 때 표시되며 iconeffect 매개 변수도 다릅니다.
seo-description: 확대/축소 표시기가 확대/축소 보기 영역에 오버레이됩니다. 이미지가 재설정 상태일 때 표시되며 iconeffect 매개 변수도 다릅니다.
seo-title: 확대/축소 보기 아이콘 효과
solution: Experience Manager
title: 확대/축소 보기 아이콘 효과
topic: Dynamic Media
uuid: 69a44789-9587-4459-9c75-048773c9e368
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 1%

---


# 확대/축소 보기 아이콘 효과{#zoom-view-icon-effect}

확대/축소 표시기가 확대/축소 보기 영역에 오버레이됩니다. 이미지가 재설정 상태일 때 표시되며 iconeffect 매개 변수도 다릅니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

보기 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> 확대/축소 표시기 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS 스프라이트 </a>를 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>확대/축소 표시기 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>확대/축소 표시기 높이. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>아이콘 효과는 다른 장치에 다른 아이콘 효과를 적용하는 데 사용할 수 있는 `media-type` 속성 선택기를 지원합니다. 특히, `media-type='standard'`은 마우스 입력이 일반적으로 사용되고 `media-type='multitouch'`은 터치 입력이 있는 장치에 해당하는 데스크톱 시스템에 해당합니다.

예 - 데스크톱 시스템 및 터치 장치에 대해 다른 아트로 100 x 100픽셀 확대/축소 표시기를 설정하려면

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```

