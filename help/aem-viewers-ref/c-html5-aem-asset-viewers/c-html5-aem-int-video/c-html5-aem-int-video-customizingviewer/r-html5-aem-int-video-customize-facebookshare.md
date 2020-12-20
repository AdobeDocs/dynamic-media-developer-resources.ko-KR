---
description: Facebook 공유 도구는 소셜 공유 패널에 추가된 단추로 구성됩니다. 단추를 클릭하면 소셜 서비스에서 제공하는 공유 대화 상자로 리디렉션됩니다. 단추의 위치는 소셜 공유 도구에 의해 완전히 관리됩니다.
seo-description: Facebook 공유 도구는 소셜 공유 패널에 추가된 단추로 구성됩니다. 단추를 클릭하면 소셜 서비스에서 제공하는 공유 대화 상자로 리디렉션됩니다. 단추의 위치는 소셜 공유 도구에 의해 완전히 관리됩니다.
seo-title: Facebook 공유
solution: Experience Manager
title: Facebook 공유
topic: Dynamic media
uuid: 6f7e9700-19c2-441d-a0d0-5bc30a50b0e3
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Facebook 공유{#facebook-share}

Facebook 공유 도구는 소셜 공유 패널에 추가된 단추로 구성됩니다. 단추를 클릭하면 소셜 서비스에서 제공하는 공유 대화 상자로 리디렉션됩니다. 단추의 위치는 소셜 공유 도구에 의해 완전히 관리됩니다.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Facebook 공유 버튼의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7facebookshare
```

**Facebook 공유 도구의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>단추 폭. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>단추 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 안에 배치할 수 있습니다. </p> <p><a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS 스프라이트 </a>를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하므로 다른 버튼 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

CSS 클래스에서 `display:none` CSS 속성을 설정하여 소셜 공유 패널에서 단추를 제거할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. [사용자 인터페이스 요소 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

## 예 {#section-01cbe0096b1443e0a7d91956bd264465}

28 x 28픽셀인 Facebook 공유 단추를 설정하고 4개의 서로 다른 단추 상태에 대해 다른 이미지를 표시하려면:

```
.s7interactivevideoviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7interactivevideoviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7interactivevideoviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```

