---
title: 이미지 맵 효과
description: 모드 매개 변수의 값에 따라 뷰어는 Dynamic Media Classic에서 맵이 처음 작성된 위치에 기본 보기 위에 이미지 맵 아이콘을 표시하거나 원본 이미지 맵의 모양과 일치하는 정확한 영역을 렌더링합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 873fc387-1d2a-4d74-b85e-fcbb13b691c5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 1%

---

# 이미지 맵 효과{#image-map-effect}

모드 매개 변수의 값에 따라 뷰어는 Dynamic Media Classic에서 맵이 처음 작성된 위치에 기본 보기 위에 이미지 맵 아이콘을 표시하거나 원본 이미지 맵의 모양과 일치하는 정확한 영역을 렌더링합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

이미지 맵 아이콘의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>다음 `s7mapoverlay` 과거의 이미지 맵 아이콘에 스타일을 지정하는 데 사용된 CSS 클래스는 이제 더 이상 사용되지 않습니다. `s7icon` 대신,

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
   <td colname="col2"> <p>이미지 맵 아이콘 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p>참조: <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>이미지 맵 아이콘 너비(픽셀 단위). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>이미지 맵 아이콘 높이(픽셀 단위). </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이미지 맵 아이콘은 `state` 속성 선택기: 의 아이콘 상태에 다양한 스킨을 적용하는 데 사용할 수 있습니다. `default` 및 `active`.

예 - 서로 다른 두 아이콘 상태에 대해 각각 다른 이미지를 표시하는 28 x 28픽셀 이미지 맵 아이콘을 설정합니다.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

참조: [이미지 맵 지원](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

다음 CSS 클래스 선택기를 사용하여 이미지 맵 영역의 모양이 제어됩니다.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 </span> </p> </td> 
   <td colname="col2"> <p> 이미지 맵 영역 채우기 색입니다. </p> <p>#RRGGBB, RGB(R,G,B) 또는 RGBA(R,G,B,A) 형식으로 지정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 이미지 맵 영역 채우기 색입니다. </p> <p>#RRGGBB, RGB(R,G,B) 또는 RGBA(R,G,B,A) 형식으로 지정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p> 이미지 맵 영역 테두리 스타일입니다. </p> <p>다음으로 지정됨 <span class="codeph"> <span class="varname"> 폭 </span> 단색 <span class="varname"> 색상 </span> </span>, 여기서 <span class="codeph"> <span class="varname"> 폭 </span> </span> 픽셀 단위로 표시되며 <span class="codeph"> <span class="varname"> 색상 </span> </span> 는 #RRGGBB, RGB(R,G,B) 또는 RGBA(R,G,B,A)로 설정됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 를 사용하여 투명한 이미지 맵 영역 설정 `1` 픽셀 검정 테두리:

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
