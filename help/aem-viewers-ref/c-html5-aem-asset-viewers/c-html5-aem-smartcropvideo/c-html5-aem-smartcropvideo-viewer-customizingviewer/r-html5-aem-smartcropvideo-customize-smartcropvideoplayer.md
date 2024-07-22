---
title: 비디오 플레이어
description: 스마트 자르기 비디오 플레이어는 비디오 컨텐츠가 뷰어 내에 표시되는 사각형 영역입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 비디오 플레이어{#video-player}

스마트 자르기 비디오 플레이어는 비디오 컨텐츠가 뷰어 내에 표시되는 사각형 영역입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

재생 중인 비디오의 크기가 스마트 자르기 비디오 플레이어의 크기와 일치하지 않으면 비디오 컨텐츠가 스마트 자르기 비디오 플레이어의 사각형 표시 영역 내에서 가운데에 표시됩니다.

다음 CSS 클래스 선택기는 스마트 자르기 비디오 플레이어의 모양을 제어합니다.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

스마트 자르기 비디오 플레이어의 **CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>기본 보기의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

시스템에서 비디오를 재생할 수 없는 경우 표시되는 오류 메시지는 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 지역화](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)를 참조하십시오.

예 - 스마트 자르기 비디오 플레이어 크기가 512 x 288픽셀로 설정된 스마트 자르기 비디오 뷰어를 설정하려면 다음을 수행하십시오.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

폐쇄 캡션은 스마트 자르기 비디오 플레이어 내부의 내부 컨테이너에 저장됩니다. 해당 컨테이너의 위치는 지원되는 WebVTT 위치 지정 연산자에 의해 제어됩니다. 캡션 텍스트 자체는 해당 컨테이너 내에 있으며 해당 스타일은 다음 CSS 클래스 선택기로 제어됩니다.

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**자막의 CSS 속성**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>닫힌 캡션 텍스트 배경 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 색 </span> </p> </td> 
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

예 - 반투명 검은색 배경에 대해 닫힌 캡션 텍스트를 14픽셀, 밝은 회색, Arial®로 설정하려면 다음을 수행합니다.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

다음 CSS 클래스 선택기를 사용하여 버퍼링 애니메이션의 모양이 제어됩니다.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
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
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
