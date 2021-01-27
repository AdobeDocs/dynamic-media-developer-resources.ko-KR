---
description: 이 단추를 클릭하거나 탭하면 사용자가 카탈로그의 마지막 페이지로 이동합니다. 이 단추는 데스크톱 시스템 및 태블릿의 주 컨트롤 표시줄에 나타납니다.휴대 전화에서는 보조 컨트롤 막대에 추가됩니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고 위치를 지정할 수 있습니다.
seo-description: 이 단추를 클릭하거나 탭하면 사용자가 카탈로그의 마지막 페이지로 이동합니다. 이 단추는 데스크톱 시스템 및 태블릿의 주 컨트롤 표시줄에 나타납니다.휴대 전화에서는 보조 컨트롤 막대에 추가됩니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고 위치를 지정할 수 있습니다.
seo-title: 마지막 페이지 단추
solution: Experience Manager
title: 마지막 페이지 단추
topic: Dynamic Media
uuid: 4cdcd2b7-a6d3-48c0-ba65-5339d232a954
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---


# 마지막 페이지 단추{#last-page-button}

이 단추를 클릭하거나 탭하면 사용자가 카탈로그의 마지막 페이지로 이동합니다. 이 단추는 데스크톱 시스템 및 태블릿의 주 컨트롤 표시줄에 나타납니다.휴대 전화에서는 보조 컨트롤 막대에 추가됩니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고 위치를 지정할 수 있습니다.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7lastpagebutton .s7panleftbutton`

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
   <td colname="col2"> <p>패딩을 포함하여 기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대 전화의 경우)의 위쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대 전화의 경우)의 오른쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대 전화의 경우)의 왼쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>패딩을 포함하여 기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대 전화의 경우)의 아래쪽 테두리에서 배치합니다. </p> </td> 
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
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 28 x 28픽셀인 마지막 페이지 단추를 설정하고, 기본 컨트롤 막대의 왼쪽 가장자리에서 4픽셀, 왼쪽 가장자리에서 220픽셀을 배치하여 4개의 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시합니다.

```
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton { 
bottom:4px; 
right:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/LastPageButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/LastPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/LastPageButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/LastPageButton_dark_disabled.png); 
}
```

