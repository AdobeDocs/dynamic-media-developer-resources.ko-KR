---
title: 소셜 공유
description: 소셜 공유 도구는 기본적으로 왼쪽 상단 모서리에 나타납니다. 사용자가 버튼을 클릭하거나 탭하면 확장되는 버튼과 패널로 구성되어 있으며, 개별 공유 도구가 포함되어 있다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5cac6c86-08fb-46fd-bab0-ab77154eb770
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# 소셜 공유{#social-share}

소셜 공유 도구는 기본적으로 왼쪽 상단 모서리에 나타납니다. 사용자가 버튼을 클릭하거나 탭하면 확장되는 버튼과 패널로 구성되어 있으며, 개별 공유 도구가 포함되어 있다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

뷰어 사용자 인터페이스에서 소셜 공유 도구의 위치 및 크기는 다음과 같이 제어됩니다.

```
.s7ecatalogsearchviewer .s7socialshare
```

**소셜 공유 도구의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-상단 </span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대의 위쪽에 있는 오프셋입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백=왼쪽 </span> </p> </td> 
   <td colname="col2"> <p> 왼쪽에 있는 다음 단추까지의 거리 또는 이 단추가 행의 첫 번째 단추인 경우 컨트롤 막대의 왼쪽입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 소셜 공유 도구의 폭입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p>소셜 공유 도구의 높이입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 맨 위에서 4픽셀, 뷰어 컨테이너 오른쪽에서 5픽셀 사이에 위치하고 28 x 28픽셀로 크기가 조정되는 소셜 공유 도구를 설정합니다.

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

소셜 공유 도구 단추의 모양은 다음 CSS 클래스 선택기로 제어합니다.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

**소셜 단추의 CSS 속성**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
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

단추 도구 설명을 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)를 참조하십시오.

예 - 4개의 서로 다른 버튼 상태에 대해 각각 다른 이미지를 표시하는 소셜 공유 도구 버튼을 설정합니다.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

개별 소셜 공유 아이콘이 포함된 패널의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
```

소셜 공유 패널의 **CSS 속성**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>패널의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 패널을 투명한 색상으로 설정합니다.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
