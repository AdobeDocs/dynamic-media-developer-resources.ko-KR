---
description: 이 단추를 클릭하거나 탭하면 기본 보기의 이미지가 확대됩니다. 이 단추는 주 제어 막대에 표시됩니다. 화면 공간을 저장하기 위해 이 단추가 휴대폰에 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고 위치를 지정할 수 있습니다.
seo-description: 이 단추를 클릭하거나 탭하면 기본 보기의 이미지가 확대됩니다. 이 단추는 주 제어 막대에 표시됩니다. 화면 공간을 저장하기 위해 이 단추가 휴대폰에 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고 위치를 지정할 수 있습니다.
seo-title: 확대 단추
solution: Experience Manager
title: 확대 단추
topic: Dynamic Media
uuid: 21f9223a-382c-49cc-afdd-2dbf703bc242
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 2%

---


# 확대 단추{#zoom-in-button}

이 단추를 클릭하거나 탭하면 기본 보기의 이미지가 확대됩니다. 이 단추는 주 제어 막대에 표시됩니다. 화면 공간을 저장하기 위해 이 단추가 휴대폰에 표시되지 않습니다. CSS를 사용하여 이 단추의 크기를 조정하고, 스킨을 지정하고 위치를 지정할 수 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**기본 뷰어 영역의 CSS 속성**

버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7zoominbutton`

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
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)의 현지화를 참조하십시오.

예 - 28 x 28픽셀의 확대 단추, 기본 컨트롤 막대의 오른쪽 가장자리에서 4 픽셀, 103픽셀의 픽셀 위치를 지정하고, 4개의 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시하려면 이 단추를 설정합니다.

```
.s7ecatalogsearchviewer .s7zoominbutton { 
bottom:4px; 
right:103px; 
width:28px; 
height:28px; 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='up'] { 
background-image:url(images/v2/ZoomInButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7zoominbutton [state='disabled'] { 
background-image:url(images/v2/ZoomInButton_dark_disabled.png); 
}
```

