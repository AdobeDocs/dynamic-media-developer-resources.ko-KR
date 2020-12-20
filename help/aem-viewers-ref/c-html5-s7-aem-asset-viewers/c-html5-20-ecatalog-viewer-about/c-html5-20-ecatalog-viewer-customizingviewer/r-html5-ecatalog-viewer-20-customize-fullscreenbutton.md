---
description: 사용자가 클릭할 때 뷰어가 전체 화면 모드로 들어가거나 종료됩니다. 이 단추는 주 제어 막대에 표시됩니다. 뷰어가 팝업 모드에서 작동하고 시스템이 기본 전체 화면을 지원하지 않는 경우 이 단추가 표시되지 않습니다. CSS로 버튼의 크기를 조정하고 스킨 후 위치를 지정할 수 있습니다.
seo-description: 사용자가 클릭할 때 뷰어가 전체 화면 모드로 들어가거나 종료됩니다. 이 단추는 주 제어 막대에 표시됩니다. 뷰어가 팝업 모드에서 작동하고 시스템이 기본 전체 화면을 지원하지 않는 경우 이 단추가 표시되지 않습니다. CSS로 버튼의 크기를 조정하고 스킨 후 위치를 지정할 수 있습니다.
seo-title: 전체 화면 단추
solution: Experience Manager
title: 전체 화면 단추
topic: Dynamic media
uuid: 1ee32e71-78bc-4cb2-858c-083c750ff1c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---


# 전체 화면 단추{#full-screen-button}

사용자가 클릭할 때 뷰어가 전체 화면 모드로 들어가거나 종료됩니다. 이 단추는 주 제어 막대에 표시됩니다. 뷰어가 팝업 모드에서 작동하고 시스템이 기본 전체 화면을 지원하지 않는 경우 이 단추가 표시되지 않습니다. CSS로 버튼의 크기를 조정하고 스킨 후 위치를 지정할 수 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col2"> <p>패딩과 같은 기본 컨트롤 막대의 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩과 같은 기본 컨트롤 막대의 오른쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩과 같은 기본 컨트롤 막대의 왼쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>패딩과 같은 기본 컨트롤 막대의 아래쪽 테두리에서 위치를 지정합니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 및 `selected` 속성 선택기를 모두 지원합니다. 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다. 특히 `selected='true'`은 &quot;전체 화면&quot; 상태에 해당하고 `selected='false'`은 &quot;정상&quot; 상태에 해당합니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 28 x 28픽셀인 전체 화면 단추를 설정하고, 기본 컨트롤 막대의 오른쪽 가장자리에서 4픽셀, 오른쪽 가장자리에서 5픽셀을 배치하여 선택 또는 선택하지 않을 경우 4개의 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시합니다.

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

