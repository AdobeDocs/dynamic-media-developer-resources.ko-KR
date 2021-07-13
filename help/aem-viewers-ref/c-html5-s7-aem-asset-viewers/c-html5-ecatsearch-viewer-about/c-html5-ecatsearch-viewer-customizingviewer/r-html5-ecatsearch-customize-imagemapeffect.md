---
description: 모드 매개 변수의 값에 따라 뷰어는 원래 Dynamic Media Classic에서 지도가 작성된 위치에 기본 보기 위에 이미지 맵 아이콘을 표시하거나 원래 이미지 맵의 모양과 일치하는 정확한 영역을 렌더링합니다.
solution: Experience Manager
title: 이미지 맵 효과
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog 검색
role: Developer,User
exl-id: 873fc387-1d2a-4d74-b85e-fcbb13b691c5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# 이미지 맵 효과{#image-map-effect}

모드 매개 변수의 값에 따라 뷰어는 원래 Dynamic Media Classic에서 지도가 작성된 위치에 기본 보기 위에 이미지 맵 아이콘을 표시하거나 원래 이미지 맵의 모양과 일치하는 정확한 영역을 렌더링합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

이미지 맵 아이콘의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>과거에 이미지 맵 아이콘의 스타일을 지정하는 데 사용된 `s7mapoverlay` CSS 클래스는 이제 사용되지 않습니다. 대신 `s7icon` 를 사용하십시오.

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
   <td colname="col2"> <p>이미지 맵 아이콘 아트웍입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>도 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>이미지 맵 아이콘 너비(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>이미지 맵 아이콘 높이(픽셀 단위)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이미지 맵 아이콘은 `state` 속성 선택기를 지원합니다. 이 선택기는 다른 스킨을 `default` 및 `active`의 아이콘 상태에 적용하는 데 사용할 수 있습니다.

예 - 두 개의 서로 다른 아이콘 상태에 대해 다른 이미지를 표시하는 28 x 28픽셀 이미지 맵 아이콘을 설정합니다.

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

[이미지 맵 지원](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)도 참조하십시오.

이미지 맵 영역의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> 배경  </span> </p> </td> 
   <td colname="col2"> <p> 이미지 맵 영역 채우기 색입니다. </p> <p>#RRGGBB, RGB(R, G, B) 또는 RGBA(R,G,B,A) 형식으로 지정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p> 이미지 맵 영역 채우기 색입니다. </p> <p>#RRGGBB, RGB(R,G,B) 또는 RGBA(R,G,B,A) 형식으로 지정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p> 이미지 맵 영역 테두리 스타일입니다. </p> <p><span class="codeph"> <span class="varname"> 너비 </span> 솔리드 <span class="varname"> 색상 </span> </span> 로 지정되며, 여기서 <span class="codeph"> <span class="varname"> 너비 </span> </span>은 픽셀로 표현되고 <span class="codeph"> <span class="varname"> 색상 </span> </span>는 #RRGGBB, RGB(R,G,B) 또는 RR(G,B,A)로 설정됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - `1` 픽셀 검정색 테두리가 있는 투명한 이미지 맵 영역을 설정합니다.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
