---
title: 아이콘 효과
description: 확대/축소 표시기가 기본 보기 영역에 오버레이됩니다. 이미지가 재설정 상태일 때 표시되며, 이는 iconeffect 매개 변수에도 의존합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 90877e39-04ac-4c6c-b7c9-98ffda9355f2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# 아이콘 효과{#icon-effect}

확대/축소 표시기가 기본 보기 영역에 오버레이됩니다. 이미지가 재설정 상태일 때 표시되며, 이는 iconeffect 매개 변수에도 의존합니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

다음 CSS 클래스 선택기를 사용하여 보기 영역의 모양이 제어됩니다.

```
.s7ecatalogsearchviewer .s7pageview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 확대/축소 표시기 아트워크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>확대/축소 표시기 너비(픽셀 단위)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>확대/축소 표시기 높이(픽셀 단위)입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>아이콘 효과는 `media-type` 특성 선택기를 지원하며, 이 선택기를 사용하여 다른 장치에 다른 아이콘 효과를 적용할 수 있습니다. 특히 `media-type='standard'`은(는) 마우스 입력이 정상적으로 사용되는 데스크톱 시스템에 해당하며 `media-type='multitouch'`은(는) 터치 입력이 있는 장치에 해당합니다.

예 - 데스크탑 시스템 및 터치 장치에 대해 서로 다른 아트로 100x100픽셀 확대/축소 표시기를 설정합니다.

```
.s7ecatalogsearchviewer .s7pageview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7ecatalogsearchviewer .s7pageview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7ecatalogsearchviewer .s7pageview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
