---
title: 비디오 플레이어
description: 비디오 플레이어는 뷰어 내에 비디오 컨텐츠가 표시되는 사각형 영역입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2f92d76e-3104-4ad8-9426-662275492251
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---

# 비디오 플레이어{#video-player}

비디오 플레이어는 뷰어 내에 비디오 컨텐츠가 표시되는 사각형 영역입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

재생 중인 비디오의 차원이 비디오 플레이어의 차원과 일치하지 않으면 비디오 컨텐츠가 비디오 플레이어의 사각형 표시 영역 내에 중심이 됩니다.

다음 CSS 클래스 선택기는 비디오 플레이어의 모양을 제어합니다.

```
.s7mixedmediaviewer .s7videoplayer
```

**비디오 플레이어의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p> 비디오 플레이어의 배경색입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

시스템에서 비디오를 재생할 수 없는 경우 표시되는 오류 메시지를 현지화할 수 있습니다. 자세한 내용은 [사용자 인터페이스 요소의 로컬라이제이션](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) 추가 정보.

예 - 비디오 플레이어를 투명하게 만들려면:

```
.s7mixedmediaviewer .s7videoplayer { 
 background-color: transparent; 
}
```

캡션은 비디오 플레이어 내의 내부 컨테이너에 배치됩니다. 해당 컨테이너의 위치는 지원되는 WebVTT 포지셔닝 연산자에 의해 제어됩니다. 캡션 텍스트 자체가 해당 컨테이너 내에 있습니다. 이 스타일은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7videoplayer .s7caption
```

**캡션의 CSS 속성**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경색 </span> </p> </td> 
   <td colname="col2"> <p>캡션 텍스트 배경. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>캡션 텍스트 색상. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>글꼴 가중치입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>글꼴 크기입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>글꼴 패밀리. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 반투명 검정 배경에서 캡션 텍스트를 14픽셀 밝은 회색®으로 설정하려면 다음을 수행합니다.

```
.s7mixedmediaviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

버퍼링 애니메이션의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon
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
   <td colname="col2"> <p> 애니메이션 아이콘 왼쪽 여백에 아이콘 너비의 절반을 뺀 것입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 여백 상단 </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘 위쪽 여백에서 일반적으로 아이콘 높이의 절반을 뺀 값입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 배경 이미지 </span> </p> </td> 
   <td colname="col2"> <p> 아트웍을 노브. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 버퍼링 애니메이션을 101픽셀 너비로 29픽셀 높이로 설정하려면 다음을 수행합니다.

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
