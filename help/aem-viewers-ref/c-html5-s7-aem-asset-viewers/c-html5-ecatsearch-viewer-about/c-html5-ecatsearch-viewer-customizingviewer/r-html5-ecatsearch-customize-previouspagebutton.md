---
description: 이 단추를 클릭하거나 탭하면 사용자가 카탈로그의 이전 페이지로 이동합니다. 이 단추는 기본 컨트롤 막대에 표시됩니다. 화면 공간을 저장하기 위해 휴대폰에 이 단추가 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.
seo-description: 이 단추를 클릭하거나 탭하면 사용자가 카탈로그의 이전 페이지로 이동합니다. 이 단추는 기본 컨트롤 막대에 표시됩니다. 화면 공간을 저장하기 위해 휴대폰에 이 단추가 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.
seo-title: 이전 페이지 단추
solution: Experience Manager
title: 이전 페이지 단추
topic: Dynamic media
uuid: 6ba16329-ce24-4a06-970e-cfcd35a8b2f0
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 이전 페이지 단추{#previous-page-button}

이 단추를 클릭하거나 탭하면 사용자가 카탈로그의 이전 페이지로 이동합니다. 이 단추는 기본 컨트롤 막대에 표시됩니다. 화면 공간을 저장하기 위해 휴대폰에 이 단추가 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton`

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
   <td colname="col2"> <p>안쪽 여백을 포함하여 기본 컨트롤 막대의 위쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>안쪽 여백을 포함하여 기본 컨트롤 막대의 오른쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>안쪽 여백을 포함하여 기본 컨트롤 막대의 왼쪽 테두리에서 위치를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>안쪽 여백을 포함하여 기본 컨트롤 막대의 아래쪽 테두리에서 위치를 지정합니다. </p> </td> 
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

예 - 28 x 28픽셀인 이전 페이지 단추를 설정하고 기본 컨트롤 막대의 오른쪽 가장자리에서 4 픽셀과 250픽셀을 배치하여 4개의 서로 다른 단추 상태에 대해 다른 이미지를 표시합니다.

```
.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton { 
bottom:4px; 
left:250px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/ToolBarLeftButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/ToolBarLeftButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/ToolBarLeftButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7toolbarleftbutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/ToolBarLeftButton_dark_disabled.png); 
}
```

