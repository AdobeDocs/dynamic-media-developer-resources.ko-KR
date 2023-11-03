---
title: 사용자 인터페이스 요소의 현지화
description: 대화형 비디오 뷰어가 표시하는 특정 컨텐츠는 현지화가 적용됩니다. 이러한 콘텐츠에는 사용자 인터페이스 요소 도구 팁과 비디오가 재생될 수 없을 때 표시되는 오류 메시지가 포함됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: d293c385-d355-4d9e-9fe9-8ef35fef60bf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# 사용자 인터페이스 요소의 현지화{#localization-of-user-interface-elements}

대화형 비디오 뷰어가 표시하는 특정 컨텐츠는 현지화가 적용됩니다. 이러한 콘텐츠에는 사용자 인터페이스 요소 도구 팁과 비디오가 재생될 수 없을 때 표시되는 오류 메시지가 포함됩니다.

현지화할 수 있는 뷰어의 모든 텍스트 콘텐츠는 SYMBOL이라는 특수한 뷰어 SDK 식별자에 의해 표현됩니다. 모든 SYMBOL에는 영어 로케일에 대한 기본 연관 텍스트 값( `"en"`) 기본 제공 뷰어와 함께 제공됩니다. 또한 필요한 수만큼 로케일에 대해 사용자 정의 값이 설정되어 있을 수 있습니다.

뷰어가 시작되면 현재 로케일을 확인하여 해당 로케일에 대해 지원되는 각 SYMBOL에 대한 사용자 정의 값이 있는지 확인합니다. 있는 경우 사용자 정의 값을 사용하고, 그렇지 않은 경우 기본 텍스트로 돌아갑니다.

사용자 정의 로컬라이제이션 데이터를 로컬라이제이션 JSON 개체로 뷰어에 전달할 수 있습니다. 이러한 객체에는 지원되는 로케일 목록, 각 로케일에 대한 SYMBOL 텍스트 값 및 기본 로케일이 포함됩니다.

이러한 현지화 객체의 예는 다음과 같습니다.

```
{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

위의 예에서 현지화 개체는 두 개의 로케일( `"en"` 및 `"fr"`)에서 각 로케일의 두 가지 사용자 인터페이스 요소에 대한 현지화 기능을 제공합니다.

웹 페이지 코드는 로컬라이제이션 개체를 뷰어 생성자에 값으로 전달해야 합니다. `localizedTexts` 구성 객체의 필드입니다. 다른 옵션은 를 호출하여 현지화 개체를 전달하는 것입니다. `setLocalizedTexts(localizationInfo)` 메서드를 사용합니다.

지원되는 기호는 다음과 같습니다.

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>기호 </p> </th> 
   <th colname="col2" class="entry"> <p>다음에 대한 도구 설명... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>최상위 뷰어 요소에 대한 ARIA 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLS_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> 재생 일시 중지 단추 상태를 선택했습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>재생 일시 중지 단추 상태를 선택 해제했습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_PLAY </span> </p> </td> 
   <td colname="col2"> <p> 재생 재생 일시 중지 단추 상태. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOL팁 </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대의 비디오 시간입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> 선택한 변경 가능한 볼륨. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>변경 가능한 볼륨을 선택 해제했습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p> ARIA를 통해 노출된 볼륨 슬라이더 노브 레이블 <span class="codeph"> aria-valuetext </span> 특성. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLS_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>정상 상태의 전체 화면 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLS_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>전체 화면 상태의 전체 화면 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p> 선택한 닫힌 캡션 단추 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p> 선택 취소된 닫힌 캡션 단추 상태. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InteractiveSwatches.BANNER </span> </p> </td> 
   <td colname="col2"> <p>배너용 캡션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>위로 스크롤 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>아래로 스크롤 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>소셜 공유 도구입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>링크 공유 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>링크 대화 상자 헤더. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>링크 대화 상자 오른쪽 위 닫기 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>공유 링크에 대한 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>취소 단추의 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLS_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>취소 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>모두 선택 단추의 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> 모두 선택 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Facebook 공유 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Twitter 공유 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>콜 투 액션 패널 닫기 버튼. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.오류 </span> </p> </td> 
   <td colname="col2"> <p>비디오 재생이 가능하지 않을 때 표시되는 오류 메시지. </p> </td> 
  </tr> 
 </tbody> 
</table>
