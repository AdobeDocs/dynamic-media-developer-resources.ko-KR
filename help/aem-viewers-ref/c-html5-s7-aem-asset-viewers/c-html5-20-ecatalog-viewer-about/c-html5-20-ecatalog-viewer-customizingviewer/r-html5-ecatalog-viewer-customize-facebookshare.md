---
title: Facebook 공유
description: Facebook 공유 도구는 소셜 공유 패널에 추가된 단추로 구성됩니다. 버튼을 선택하면 사용자가 소셜 서비스에서 제공하는 공유 대화 상자로 리디렉션됩니다. 버튼의 위치는 소셜 공유 도구에서 완전히 관리됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 0525bfd0-ce38-4fd1-a5cc-e6b5acab1651
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Facebook 공유{#facebook-share}

Facebook 공유 도구는 소셜 공유 패널에 추가된 단추로 구성됩니다. 버튼을 선택하면 사용자가 소셜 서비스에서 제공하는 공유 대화 상자로 리디렉션됩니다. 버튼의 위치는 소셜 공유 도구에서 완전히 관리됩니다.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Facebook 공유 단추의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7facebookshare
```

**Facebook 공유 도구의 CSS 속성**

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
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 배치합니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS 스프라이트 </a>도 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 특성 선택기를 지원하며, 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

CSS 클래스에서 `display:none` CSS 속성을 설정하여 소셜 공유 패널에서 단추를 제거할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

예 - 28 x 28픽셀인 Facebook 공유 단추를 설정하고 4개의 다른 단추 상태 각각에 대해 다른 이미지를 표시하려면:

```
.s7ecatalogviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
