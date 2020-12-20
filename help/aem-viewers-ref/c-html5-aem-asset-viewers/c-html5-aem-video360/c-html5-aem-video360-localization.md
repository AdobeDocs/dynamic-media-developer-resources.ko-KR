---
description: 뷰어가 표시하는 특정 컨텐츠는 현지화를 따릅니다. 여기에는 사용자 인터페이스 요소 도구 설명 및 비디오가 재생되지 않을 때 표시되는 오류 메시지가 포함됩니다.
seo-description: 뷰어가 표시하는 특정 컨텐츠는 현지화를 따릅니다. 여기에는 사용자 인터페이스 요소 도구 설명 및 비디오가 재생되지 않을 때 표시되는 오류 메시지가 포함됩니다.
seo-title: 사용자 인터페이스 요소의 로컬라이제이션
solution: Experience Manager
title: 사용자 인터페이스 요소의 로컬라이제이션
topic: Dynamic media
uuid: d5e75af0-03d6-4357-a540-4094313ed026
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# 사용자 인터페이스 요소의 현지화{#localization-of-user-interface-elements}

뷰어가 표시하는 특정 컨텐츠는 현지화를 따릅니다. 여기에는 사용자 인터페이스 요소 도구 설명 및 비디오가 재생되지 않을 때 표시되는 오류 메시지가 포함됩니다.

지역화할 수 있는 뷰어의 모든 텍스트 컨텐츠는 SYMBOL이라는 특수 뷰어 SDK 식별자로 표시됩니다. 모든 SYMBOL은 기본 뷰어와 함께 제공된 영어 로케일( `"en"`)에 대한 기본 관련 텍스트 값을 갖습니다. 필요에 따라 많은 로캘에 대해 사용자 정의 값이 설정될 수도 있습니다.

뷰어가 시작되면 지원되는 각 SYMBOL의 로케일 사용자 정의 값이 있는지 여부를 확인하기 위해 현재 로케일을 확인합니다. 있는 경우 사용자 정의 값을 사용합니다.그렇지 않으면 기본 텍스트로 돌아갑니다.

사용자 정의 현지화 데이터는 로컬라이제이션 JSON 개체로서 뷰어에 전달할 수 있습니다. 이러한 객체에는 지원되는 로케일 목록, 각 로케일에 대한 SYMBOL 텍스트 값 및 기본 로캘이 포함되어 있습니다.

이러한 현지화 객체의 예는 다음과 같습니다.

```
{ 
"en":{ 
"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

위의 예에서 현지화 객체는 두 로케일( `"en"` 및 `"fr"`)을 정의하고 각 로케일에서 두 사용자 인터페이스 요소에 대한 현지화를 제공합니다.

웹 페이지 코드는 구성 객체의 `localizedTexts` 필드 값으로 로컬라이제이션 객체를 뷰어 생성자에 전달해야 합니다. 대체 옵션은 `setLocalizedTexts(localizationInfo)` 메서드를 호출하여 현지화 개체를 전달하는 것입니다.

다음 심볼이 지원됩니다.

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>심볼 </p> </th> 
   <th colname="col2" class="entry"> <p>툴팁 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>최상위 뷰어 요소에 대한 ARIA 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>선택한 재생 일시 정지 단추 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>[재생 일시 정지] 단추 상태를 선택 해제했습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY  </span> </p> </td> 
   <td colname="col2"> <p>[일시 정지] 단추 상태를 재생합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 모음에서 비디오 시간. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MUTABLEVolume.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>선택한 변경 가능한 볼륨 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MUTABLEVolume.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>선택 해제되어 있는 볼륨. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME  </span> </p> </td> 
   <td colname="col2"> <p>볼륨 슬라이더 노브 레이블은 ARIA <span class="codeph"> aria-valueext </span> 특성을 통해 노출됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>일반 상태의 전체 화면 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>전체 화면 상태의 전체 화면 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>소셜 공유 툴. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>공유 포함 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>포함 대화 상자 헤더입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>포함 대화 상자의 오른쪽 위 닫기 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>포함 코드 텍스트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>포함 크기 콤보 상자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>"취소" 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>"취소" 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>"모두 선택" 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP 작업  </span> </p> </td> 
   <td colname="col2"> <p>"모두 선택" 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE  </span> </p> </td> 
   <td colname="col2"> <p>포함 크기 콤보 상자의 마지막 "사용자 정의 크기" 항목입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>링크 공유 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>링크 대화 상자 헤더입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>링크 대화 상자의 오른쪽 위 닫기 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>공유 링크. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>"취소" 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>"취소" 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>"모두 선택" 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LINKShare.TOOLTIP 작업  </span> </p> </td> 
   <td colname="col2"> <p>"모두 선택" 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Facebook 공유 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Twitter 공유 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Video360Player.ERROR  </span> </p> </td> 
   <td colname="col2"> <p>비디오를 재생할 수 없을 때 표시되는 오류 메시지입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

