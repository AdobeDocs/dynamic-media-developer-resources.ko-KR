---
description: 모드 매개 변수의 값에 따라 뷰어는 맵을 원래 Scene7 Publishing System에서 만든 위치에서 기본 보기 위에 이미지 맵 아이콘을 표시하거나 원본 이미지 맵의 모양과 일치하는 정확한 영역을 렌더링합니다.
seo-description: 모드 매개 변수의 값에 따라 뷰어는 맵을 원래 Scene7 Publishing System에서 만든 위치에서 기본 보기 위에 이미지 맵 아이콘을 표시하거나 원본 이미지 맵의 모양과 일치하는 정확한 영역을 렌더링합니다.
seo-title: 이미지 맵 효과
solution: Experience Manager
title: 이미지 맵 효과
topic: Dynamic media
uuid: 8bafaec3-500c-4a1f-b511-bff125daab7f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 1%

---


# 이미지 맵 효과{#image-map-effect}

모드 매개 변수의 값에 따라 뷰어는 맵을 원래 Scene7 Publishing System에서 만든 위치에서 기본 보기 위에 이미지 맵 아이콘을 표시하거나 원본 이미지 맵의 모양과 일치하는 정확한 영역을 렌더링합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

이미지 맵 아이콘의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>이전에는 이미지 맵 아이콘의 스타일을 지정하는 데 사용된 `s7mapoverlay` CSS 클래스가 더 이상 사용되지 않습니다.대신 `s7icon`을(를) 사용하십시오.

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
   <td colname="col2"> <p>이미지 맵 아이콘 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
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
>이미지 맵 아이콘은 `state` 속성 선택기를 지원합니다. 이 선택기는 `default` 및 `active`의 아이콘 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

예 - 서로 다른 두 아이콘 상태에 대해 서로 다른 이미지를 표시하는 28 x 28 픽셀 이미지 맵 아이콘을 설정합니다.

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

이미지 맵 영역의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col2"> <p> 이미지 맵 영역 채우기 색상입니다. </p> <p>#RRGGBB, RGB(R,G,B) 또는 RGBA(R,G,B,A) 형식으로 지정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 이미지 맵 영역 채우기 색상입니다. </p> <p>#RRGGBB, RGB(R,G,B) 또는 RGBA(R,G,B,A) 형식으로 지정됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 경계 </span> </p> </td> 
   <td colname="col2"> <p> 이미지 맵 영역 테두리 스타일입니다. </p> <p><span class="codeph"> <span class="varname"> 너비 </span> 단색 <span class="varname"> 색상 </span> </span>로 지정됨. 여기서 <span class="codeph"> <span class="varname"> 너비 </span> </span>은 픽셀로 표현되고 <span class="codeph"> <span class="varname"> 색상 </span> </span> 는 으로 설정됩니다. #RRGGBB, RGB(R,G,B) 또는 RGBA(R,G,B,A) </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - `1` 픽셀 검정 테두리로 투명 이미지 맵 영역을 설정합니다.

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

