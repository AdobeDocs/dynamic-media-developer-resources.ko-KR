---
description: 이 단추를 클릭하거나 탭하면 사용자가 카탈로그의 첫 페이지로 이동합니다. 이 단추는 데스크톱 시스템 및 태블릿의 기본 제어 표시줄에 나타납니다. 휴대폰에서는 보조 컨트롤 모음에 추가됩니다. CSS를 사용하여 이 단추의 크기를 지정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.
solution: Experience Manager
title: 첫 번째 페이지 단추
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog 검색
role: Developer,User
exl-id: a84c8b20-93ea-4121-99b0-427e45ec0417
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 2%

---

# 첫 번째 페이지 단추{#first-page-button}

이 단추를 클릭하거나 탭하면 사용자가 카탈로그의 첫 페이지로 이동합니다. 이 단추는 데스크톱 시스템 및 태블릿의 기본 제어 표시줄에 나타납니다. 휴대폰에서는 보조 컨트롤 모음에 추가됩니다. CSS를 사용하여 이 단추의 크기를 지정하고, 스킨을 지정하고, 위치를 지정할 수 있습니다.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton`

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
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대폰의 경우)의 위쪽 테두리에서 패딩을 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대폰의 경우)의 오른쪽 테두리에서 패딩을 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대폰의 경우)(패딩 포함)의 왼쪽 테두리에서 배치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대(데스크톱 시스템 및 태블릿의 경우) 또는 보조 컨트롤 막대(휴대폰의 경우)의 안쪽 테두리에서 패딩을 배치합니다. </p> </td> 
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
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하며, 이 선택기를 사용하여 다른 스킨을 다른 단추 상태에 적용할 수 있습니다.

단추 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소 현지화](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

예 - 28 x 28픽셀인 첫 번째 페이지 단추를 설정하려면 맨 아래쪽에서 4픽셀이고 기본 컨트롤 막대의 왼쪽 가장자리에서 220픽셀입니다. 또한 네 개의 서로 다른 단추 상태에 대해 다른 이미지를 표시합니다.

```
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton { 
bottom:4px; 
left:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/FirstPageButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/FirstPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/FirstPageButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7firstpagebutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/FirstPageButton_dark_disabled.png); 
}
```
