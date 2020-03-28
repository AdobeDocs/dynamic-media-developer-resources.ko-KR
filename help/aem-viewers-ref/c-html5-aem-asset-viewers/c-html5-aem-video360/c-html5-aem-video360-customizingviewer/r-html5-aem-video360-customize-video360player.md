---
description: 비디오 플레이어는 뷰어 내에 비디오 컨텐츠가 표시되는 사각형 영역입니다.
seo-description: 비디오 플레이어는 뷰어 내에 비디오 컨텐츠가 표시되는 사각형 영역입니다.
seo-title: Video360 플레이어
solution: Experience Manager
title: Video360 플레이어
topic: Dynamic media
uuid: e78a9c22-4217-42cc-ba47-3acb4130a4fd
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video360 player{#video-player}

비디오 플레이어는 뷰어 내에 비디오 컨텐츠가 표시되는 사각형 영역입니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

재생되는 비디오 크기가 비디오 플레이어의 크기와 일치하지 않는 경우 비디오 컨텐츠의 가운데가 비디오 플레이어의 사각형 표시 영역 내에 있습니다.

다음 CSS 클래스 선택기는 비디오 플레이어의 모양을 제어합니다.

```
.s7video360viewer .s7video360player
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

시스템에서 비디오를 재생할 수 없는 경우 표시되는 오류 메시지를 현지화할 수 있습니다.

사용자 [인터페이스 요소의](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)현지화를 참조하십시오.

예 - 비디오 플레이어 크기가 512 x 288픽셀로 설정된 비디오 뷰어를 설정하려면

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

버퍼링 애니메이션의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘 너비. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘 높이. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘의 왼쪽 여백에서 일반적으로 아이콘 너비의 절반을 뺀 값입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> 애니메이션 아이콘 위쪽 여백으로서, 일반적으로 아이콘 높이의 절반을 뺀 것입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 아트웍을 조절합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 버퍼링 애니메이션을 너비 101픽셀, 높이 29픽셀로 설정하려면

```
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

