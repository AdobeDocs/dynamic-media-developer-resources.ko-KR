---
title: 비디오 플레이어
description: 비디오 플레이어는 비디오 컨텐츠가 뷰어 내에 표시되는 사각형 영역입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 54ccf872-2d24-4d3f-9808-6d0e2558f5a5
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# 비디오 플레이어{#video-player}

비디오 플레이어는 비디오 컨텐츠가 뷰어 내에 표시되는 사각형 영역입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

재생 중인 비디오의 치수가 비디오 플레이어의 치수와 일치하지 않으면 비디오 컨텐츠가 비디오 플레이어의 사각형 표시 영역 내에서 가운데에 표시됩니다.

다음 CSS 클래스 선택기는 비디오 플레이어의 모양을 제어합니다.

```
.s7video360viewer .s7video360player
```

비디오 플레이어의 **CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>기본 보기의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

시스템에서 비디오를 재생할 수 없는 경우에 표시되는 오류 메시지를 현지화할 수 있습니다.

[사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)을 참조하세요.

예 - 비디오 플레이어 크기를 512 x 288픽셀로 설정한 비디오 뷰어를 설정합니다.

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

다음 CSS 클래스 선택기를 사용하여 버퍼링 애니메이션의 모양이 제어됩니다.

```
.s7video360viewer .s7video360player .s7waiticon
```

**대기 아이콘의 CSS 속성**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 너비 </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 높이 </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-왼쪽 </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘의 왼쪽 여백은 일반적으로 아이콘 폭의 절반을 뺀 것입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-상단 </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘 위쪽 여백으로, 일반적으로 아이콘 높이의 절반을 뺍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 손잡이 아트워크. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 버퍼링 애니메이션을 폭 101픽셀, 높이 29픽셀로 설정하려면 다음을 수행합니다.

```
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
