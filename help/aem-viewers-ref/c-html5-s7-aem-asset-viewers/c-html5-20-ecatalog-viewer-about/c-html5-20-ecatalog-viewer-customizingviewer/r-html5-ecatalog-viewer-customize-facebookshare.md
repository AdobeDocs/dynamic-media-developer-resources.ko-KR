---
description: Facebook 공유 도구는 소셜 공유 패널에 추가된 단추로 구성됩니다. 버튼을 선택하면 사용자가 소셜 서비스에서 제공하는 공유 대화 상자로 리디렉션됩니다. 단추의 위치는 소셜 공유 도구에서 완전히 관리됩니다.
solution: Experience Manager
title: Facebook 공유
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 0525bfd0-ce38-4fd1-a5cc-e6b5acab1651
source-git-commit: fd3a1fe47da5ba26b53ea9414bfec1e4c11d7392
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# Facebook 공유{#facebook-share}

Facebook 공유 도구는 소셜 공유 패널에 추가된 단추로 구성됩니다. 버튼을 선택하면 사용자가 소셜 서비스에서 제공하는 공유 대화 상자로 리디렉션됩니다. 단추의 위치는 소셜 공유 도구에서 완전히 관리됩니다.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

facebook 공유 단추의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer .s7facebookshare
```

**facebook 공유 도구의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>단추 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치 </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p>참조 - <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기. 다른 스킨을 다른 단추 상태에 적용하는 데 사용할 수 있습니다.

Social 공유 패널에서 단추를 제거하려면 `display:none` CSS 클래스의 CSS 속성입니다.

단추 도구 팁은 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 추가 정보.

예 - 28 x 28픽셀인 Facebook 공유 단추를 설정하고 네 개의 서로 다른 단추 상태에 대해 다른 이미지를 표시하려면 다음을 수행하십시오.

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
