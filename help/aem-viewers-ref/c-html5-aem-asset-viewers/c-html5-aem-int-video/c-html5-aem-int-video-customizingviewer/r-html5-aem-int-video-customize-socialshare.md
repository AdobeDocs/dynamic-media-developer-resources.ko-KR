---
title: 소셜 공유
description: 기본적으로 소셜 공유 도구가 오른쪽 상단 모서리에 표시됩니다. 이 패널은 사용자가 단추를 클릭하거나 탭할 때 확장되는 단추와 패널이며 개별 공유 도구가 포함되어 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: ad544a12-d2a4-45c9-9e76-e0bf96901725
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 2%

---

# 소셜 공유{#social-share}

기본적으로 소셜 공유 도구가 오른쪽 상단 모서리에 표시됩니다. 이 패널은 사용자가 단추를 클릭하거나 탭할 때 확장되는 단추와 패널이며 개별 공유 도구가 포함되어 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

뷰어 사용자 인터페이스에서 소셜 공유 도구의 위치 및 크기는 다음과 같이 제어됩니다.

```
.s7interactivevideoviewer .s7socialshare
```

**소셜 공유 도구의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p> 뷰어 컨테이너를 기준으로 하는 소셜 공유 도구의 세로 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p> 뷰어 컨테이너를 기준으로 하는 소셜 공유 도구의 수평 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 소셜 공유 도구의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>소셜 공유 도구의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example}

위쪽에서 4픽셀, 뷰어 컨테이너의 오른쪽에서 5픽셀까지 배치되고 크기가 28 x 28픽셀인 소셜 공유 도구를 설정하려면 다음을 수행하십시오.

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

소셜 공유 도구 단추의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton
```

**소셜 공유 도구 단추의 CSS 속성**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지  </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 위치  </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내부에 위치를 지정합니다. </p> <p><a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a> 를 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 버튼은 `state` 속성 선택기를 지원하며, 이 선택기를 사용하여 다른 스킨을 다른 단추 상태에 적용할 수 있습니다.

단추 도구 팁은 현지화할 수 있습니다. [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)을 참조하십시오.

## 예 {#example-1}

네 개의 서로 다른 단추 상태에 대해 다른 이미지를 표시하는 소셜 공유 도구 단추를 설정하려면 다음을 수행하십시오.

```
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

개별 소셜 공유 아이콘이 포함된 패널의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel
```

**소셜 공유 패널의 CSS 속성**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색  </span> </p> </td> 
   <td colname="col2"> <p>패널의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example-2}

투명한 색상을 갖도록 패널을 설정하려면 다음을 수행하십시오.

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
