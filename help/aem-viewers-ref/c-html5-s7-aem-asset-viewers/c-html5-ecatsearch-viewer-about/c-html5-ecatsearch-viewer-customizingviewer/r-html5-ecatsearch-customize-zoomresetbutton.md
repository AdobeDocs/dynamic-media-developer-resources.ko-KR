---
description: 이 단추를 클릭하거나 탭하면 기본 보기에서 이미지가 재설정됩니다. 이 단추는 데스크톱 시스템 및 태블릿의 주 컨트롤 막대에 표시됩니다. 휴대폰의 경우 이 단추는 이미지 위에 있는 아래쪽 가운데에 표시됩니다. 그러나 이미지가 재설정 상태일 때는 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.
seo-description: 이 단추를 클릭하거나 탭하면 기본 보기에서 이미지가 재설정됩니다. 이 단추는 데스크톱 시스템 및 태블릿의 주 컨트롤 막대에 표시됩니다. 휴대폰의 경우 이 단추는 이미지 위에 있는 아래쪽 가운데에 표시됩니다. 그러나 이미지가 재설정 상태일 때는 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.
seo-title: 확대/축소 재설정 단추
solution: Experience Manager
title: 확대/축소 재설정 단추
topic: Dynamic media
uuid: 19ef5c77-8352-4021-a022-adec6ecbf078
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 확대/축소 재설정 단추{#zoom-reset-button}

이 단추를 클릭하거나 탭하면 기본 보기에서 이미지가 재설정됩니다. 이 단추는 데스크톱 시스템 및 태블릿의 주 컨트롤 막대에 표시됩니다. 휴대폰의 경우 이 단추는 이미지 위에 있는 아래쪽 가운데에 표시됩니다. 그러나 이미지가 재설정 상태일 때는 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7zoomresetbutton`

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
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 및 태블릿에 있음) 또는 뷰어(휴대폰에 있음)의 위쪽 테두리에서 패딩을 포함하여 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 및 태블릿에 있음) 또는 뷰어(휴대 전화에 있음)의 오른쪽 테두리에서 패딩을 포함하여 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>데스크톱 및 태블릿의 주 컨트롤 막대 또는 뷰어(휴대 전화의 경우)의 왼쪽 테두리에서 패딩이 포함된 위치를 지정할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 및 태블릿에서) 또는 뷰어(휴대 전화에서)의 아래쪽 테두리에서 패딩을 포함하여 위치를 지정합니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 속성 선택기를 지원합니다. 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 [내용은 사용자 인터페이스 요소의](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 현지화를 참조하십시오.

예 - 28 x 28픽셀인 확대/축소 재설정 단추를 설정하고, 기본 컨트롤 막대의 오른쪽 가장자리에서 위치(데스크톱에 있음) 4픽셀과 47픽셀을 설정하며, 서로 다른 네 가지 단추 상태 각각에 대해 다른 이미지를 표시합니다.

```
.s7ecatalogsearchviewer .s7zoomresetbutton { 
bottom:4px; 
right:47px; 
width:28px; 
height:28px; 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='up'] { 
background-image:url(images/v2/ZoomResetButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='over'] {  
background-image:url(images/v2/ZoomResettButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='down'] {  
background-image:url(images/v2/ZoomResetButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='disabled'] { 
background-image:url(images/v2/ZoomResetButton_dark_disabled.png); 
}
```

