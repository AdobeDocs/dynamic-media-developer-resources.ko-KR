---
title: 정보 패널 팝업
description: 사용자가 Dynamic Media Classic에 rollover_key 속성이 정의된 이미지 맵을 활성화할 때, 그리고 정보 패널 기능이 뷰어에 대해 올바르게 구성된 경우 정보 패널 팝업이 뷰어 영역 중간에 표시됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 907b7bd5-3f87-4918-ad62-8a28249ea023
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# 정보 패널 팝업{#info-panel-popup}

사용자가 Dynamic Media Classic에 rollover_key 속성이 정의된 이미지 맵을 활성화할 때, 그리고 정보 패널 기능이 뷰어에 대해 올바르게 구성된 경우 정보 패널 팝업이 뷰어 영역 중간에 표시됩니다.

정보 패널 배경은 전체 뷰어 영역을 포함하며 다음 CSS 클래스 선택기로 제어됩니다.

`.s7ecatalogsearchviewer .s7infopanelpopup .s7backoverlay`

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
   <td colname="col2"> <p>정보 패널 배경 채우기. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다.</p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 반투명 검은색 배경을 사용하도록 정보 패널 팝업을 설정합니다.

```
.s7ecatalogsearchviewer .s7infopanelpopup .s7backoverlay { 
 background-color : rgba(0,0,0,0.75); 
}
```

기본적으로 뷰어 영역 가운데에 정보 패널 대화 상자가 표시됩니다. 그러나 크기, 정렬, 배경 및 CSS 클래스 선택기와의 테두리를 제어할 수 있습니다.

`.s7ecatalogsearchviewer .s7infopanelpopup .s7overlay`

<table id="table_4E666A03A3D44CEEA72225113553AB3F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 남음 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 영역 패널 배경 채우기 내에서 정보 패널 대화 상자의 가로 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p>뷰어 영역 내 정보 패널 대화 상자의 세로 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>대화 상자 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>대화 상자 높이입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-왼쪽 </span> </p> </td> 
   <td colname="col2"> <p>정보 패널 대화 상자의 왼쪽 여백은 가운데 맞춤으로 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-상단 </span> </p> </td> 
   <td colname="col2"> <p>정보 패널 대화 상자의 위쪽 여백은 가운데 맞춤으로 사용할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 패딩 </span> </p> </td> 
   <td colname="col2"> <p>내부 대화 상자 패딩. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>대화 상자 배경색입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>대화 상자 테두리 반경. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상자-그림자 </span> </p> </td> 
   <td colname="col2"> <p>대화 상자 그림자. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 뷰어 영역 중앙에 300x200픽셀 정보 패널 대화 상자를 설정합니다. 이 대화 상자에는 맨 위에 40픽셀 패딩이 있고 다른 모든 면에 10픽셀 패딩이 있으며, 배경이 밝은 회색이고 테두리 반경과 그림자가 10픽셀입니다.

```
.s7ecatalogsearchviewer .s7infopanelpopup .s7overlay { 
 left: 50%; 
 top: 50%; 
 margin-left: -150px; 
 margin-top: -100px; 
 width: 300px; 
 height: 200px; 
 padding-top: 40px; 
 padding-right: 10px; 
 padding-bottom: 10px; 
 padding-left: 10px; 
 background-color:rgb(221,221,221); 
 border-radius: 10px 10px 10px 10px; 
box-shadow: 0 0 5px rgba(0,0,0,0.25);  
}
```

[정보 패널] 대화 상자에는 닫기 단추가 있으며 이 단추를 클릭하거나 탭하면 대화 상자가 닫힙니다.

이 단추의 모양은 다음 CSS 클래스 선택기로 제어합니다.

`.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 상위 </span> </p> </td> 
   <td colname="col2"> <p>대화 상자의 위쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>대화 상자의 오른쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 남음 </span> </p> </td> 
   <td colname="col2"> <p>대화 상자의 왼쪽 테두리에서 위치. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 하단 </span> </p> </td> 
   <td colname="col2"> <p>대화 상자의 아래쪽 테두리에서 위치합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p>단추 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p>지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 특성 선택기를 지원하며, 이 선택기를 사용하여 다른 단추 상태에 다른 스킨을 적용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

예 - 28x28픽셀, 정보 패널 대화 상자의 위쪽 및 오른쪽 가장자리에서 5픽셀, 서로 다른 네 개의 단추 상태 각각에 대해 다른 이미지를 표시하는 대화 상자 닫기 단추를 설정합니다.

```
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton { 
 width: 28px; 
 height: 28px; 
 top: 5px; 
 right: 5px; 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="up"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="over"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="down"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="disabled"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
}
```
