---
title: Twitter 공유
description: Twitter 공유 도구는 소셜 공유 패널에 추가된 단추로 구성됩니다. 버튼을 선택하면 사용자가 소셜 서비스에서 제공하는 공유 대화 상자로 리디렉션됩니다. 버튼의 위치는 소셜 공유 도구에서 완전히 관리됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c7e84d40-a779-4747-b79a-3a40a622a445
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Twitter 공유{#twitter-share}

Twitter 공유 도구는 소셜 공유 패널에 추가된 단추로 구성됩니다. 버튼을 선택하면 사용자가 소셜 서비스에서 제공하는 공유 대화 상자로 리디렉션됩니다. 버튼의 위치는 소셜 공유 도구에서 완전히 관리됩니다.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Twitter 공유 단추의 모양은 다음 CSS 클래스 선택기로 제어합니다.

```
.s7ecatalogsearchviewer .s7twittershare
```

**Twitter 공유 도구의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 백그라운드 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 특성 선택기를 지원하며, 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

CSS 클래스에서 `display:none` CSS 속성을 설정하여 소셜 공유 패널에서 단추를 제거할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

예 - 28 x 28픽셀인 Twitter 공유 단추를 설정하고 네 개의 서로 다른 단추 상태 각각에 대해 다른 이미지를 표시하려면 다음을 수행합니다.

```
.s7ecatalogsearchviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
