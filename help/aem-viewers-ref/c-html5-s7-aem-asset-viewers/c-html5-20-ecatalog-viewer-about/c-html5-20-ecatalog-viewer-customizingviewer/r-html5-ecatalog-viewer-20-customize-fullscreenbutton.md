---
description: 사용자가 클릭했을 때 뷰어가 전체 화면 모드로 들어가거나 종료되도록 합니다. 이 단추는 주 컨트롤 모음에 나타납니다. 뷰어가 팝업 모드에서 작동하며 시스템이 기본 전체 화면을 지원하지 않는 경우에는 이 단추가 표시되지 않습니다. CSS로 단추의 크기를 지정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.
solution: Experience Manager
title: 전체 화면 단추
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 3f56fbd2-4d2e-4cfa-bc97-350bc2bb708e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 2%

---

# 전체 화면 단추{#full-screen-button}

사용자가 클릭했을 때 뷰어가 전체 화면 모드로 들어가거나 종료되도록 합니다. 이 단추는 주 컨트롤 모음에 나타납니다. 뷰어가 팝업 모드에서 작동하며 시스템이 기본 전체 화면을 지원하지 않는 경우에는 이 단추가 표시되지 않습니다. CSS로 단추의 크기를 지정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogviewer .s7fullscreenbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대의 위쪽 테두리에서 패딩을 포함하여 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대의 오른쪽 테두리에서 패딩을 포함하여 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대의 왼쪽 테두리에서 패딩을 포함하여 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대의 아래쪽 테두리에서 패딩을 포함하여 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>단추의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>단추의 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 및 `selected` 속성 선택기를 모두 지원하며, 이 선택기는 다른 스킨(skin)을 다른 단추 상태에 적용하는 데 사용할 수 있습니다. 특히 `selected='true'`은 &quot;전체 화면&quot; 상태에 해당하고 `selected='false'`은 &quot;일반&quot; 상태에 해당합니다.

단추 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소 현지화](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

예 - 28 x 28픽셀인 전체 화면 단추를 설정하고, 기본 컨트롤 막대의 오른쪽 가장자리에서는 4픽셀과 5픽셀을 배치하며, 선택 여부에 따라 네 개의 서로 다른 단추 상태에 대해 다른 이미지를 표시합니다.

```
.s7ecatalogviewer .s7fullscreenbutton { 
bottom:4px; 
right:5px; 
width:28px; 
height:28px; 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
