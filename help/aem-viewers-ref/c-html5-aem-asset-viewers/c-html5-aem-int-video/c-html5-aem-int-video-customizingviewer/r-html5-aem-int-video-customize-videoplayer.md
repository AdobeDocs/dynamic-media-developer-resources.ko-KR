---
title: 비디오 플레이어
description: 비디오 플레이어는 비디오 컨텐츠가 뷰어 내에 표시되는 사각형 영역입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9cfeceff-f6bd-42d9-9b85-456bbaa278fd
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---

# 비디오 플레이어{#video-player}

비디오 플레이어는 비디오 컨텐츠가 뷰어 내에 표시되는 사각형 영역입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

재생 중인 비디오의 치수가 비디오 플레이어의 치수와 일치하지 않으면 비디오 컨텐츠가 비디오 플레이어의 사각형 표시 영역 내에서 가운데에 표시됩니다.

다음 CSS 클래스 선택기는 비디오 플레이어의 모양을 제어합니다.

```
.s7interactivevideoviewer .s7videoplayer
```

**비디오 플레이어의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>기본 보기의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

시스템에서 비디오를 재생할 수 없는 경우에 표시되는 오류 메시지를 현지화할 수 있습니다.

다음을 참조하십시오 [사용자 인터페이스 요소의 현지화](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

예 - 비디오 플레이어 크기를 512 x 288픽셀로 설정한 비디오 뷰어를 설정합니다.

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

폐쇄 캡션은 비디오 플레이어 내부의 내부 컨테이너에 저장됩니다. 해당 컨테이너의 위치는 지원되는 WebVTT 위치 지정 연산자에 의해 제어됩니다. 캡션 텍스트 자체는 해당 컨테이너 내에 있으며 해당 스타일은 다음 CSS 클래스 선택기로 제어됩니다.

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**폐쇄 캡션의 CSS 속성**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>닫힌 캡션 텍스트 배경 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>캡션 텍스트 색상을 닫습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p> 폐쇄 캡션 글꼴 두께. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> 자막 글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>선택 캡션 글꼴입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예 {#section-5b82913ff3c44b7b8187969cb15e9560}

반투명 검은색 배경에서 닫힌 캡션 텍스트를 14픽셀(밝은 회색, Arial®)로 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

다음 CSS 클래스 선택기를 사용하여 버퍼링 애니메이션의 모양이 제어됩니다.

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 왼쪽 여백 </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘의 왼쪽 여백은 일반적으로 아이콘 폭의 절반을 뺀 것입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백-상단 </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘 위쪽 여백으로, 일반적으로 아이콘 높이의 절반을 뺍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 손잡이 아트워크. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 버퍼링 애니메이션을 폭 101픽셀, 높이 29픽셀로 설정하려면 다음을 수행합니다.

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
