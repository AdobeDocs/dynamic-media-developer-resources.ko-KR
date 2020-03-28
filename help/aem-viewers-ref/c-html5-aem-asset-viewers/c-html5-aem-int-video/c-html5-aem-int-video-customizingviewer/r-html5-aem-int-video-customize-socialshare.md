---
description: 기본적으로 소셜 공유 도구는 오른쪽 위 모서리에 표시됩니다. 사용자가 단추를 클릭하거나 탭할 때 확장되는 버튼과 패널이며 개별 공유 도구가 포함되어 있습니다.
seo-description: 기본적으로 소셜 공유 도구는 오른쪽 위 모서리에 표시됩니다. 사용자가 단추를 클릭하거나 탭할 때 확장되는 버튼과 패널이며 개별 공유 도구가 포함되어 있습니다.
seo-title: 소셜 공유
solution: Experience Manager
title: 소셜 공유
topic: Dynamic media
uuid: 1123e96a-581f-4c1c-ad95-9804e3235002
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 소셜 공유{#social-share}

기본적으로 소셜 공유 도구는 오른쪽 위 모서리에 표시됩니다. 사용자가 단추를 클릭하거나 탭할 때 확장되는 버튼과 패널이며 개별 공유 도구가 포함되어 있습니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

뷰어 사용자 인터페이스에서 소셜 공유 도구의 위치와 크기는 다음과 같이 제어됩니다.

```
.s7interactivevideoviewer .s7socialshare
```

**소셜 공유 도구의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 최상위 </span> </p> </td> 
   <td colname="col2"> <p> 뷰어 컨테이너를 기준으로 소셜 공유 도구의 세로 위치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 </span> </p> </td> 
   <td colname="col2"> <p> 뷰어 컨테이너를 기준으로 소셜 공유 도구의 수평 위치입니다. </p> </td> 
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

위쪽에서 4픽셀, 뷰어 컨테이너의 오른쪽에서 5픽셀로 크기가 28 x 28픽셀인 소셜 공유 도구를 설정하려면

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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 지정된 단추 상태에 대해 표시되는 이미지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> CSS 스프라이트를 사용하는 경우 아트워크 스프라이트 내에서 위치를 지정할 수 있습니다. </p> <p>CSS <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 스프라이트를 참조하십시오 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>이 단추는 `state` 속성 선택기를 지원합니다. 이 선택기는 다른 단추 상태에 다른 스킨을 적용하는 데 사용할 수 있습니다.

단추 도구 설명을 현지화할 수 있습니다. 사용자 [인터페이스 요소의](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)현지화를 참조하십시오.

## 예 {#example-1}

서로 다른 네 가지 단추 상태에 대해 서로 다른 이미지를 표시하는 소셜 공유 도구 단추를 설정하려면

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>패널의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#example-2}

투명한 색상을 갖도록 패널을 설정하려면

```
.s7interactivevideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

