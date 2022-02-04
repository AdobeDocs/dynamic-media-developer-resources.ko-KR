---
title: 사용자 인터페이스 요소의 로컬라이제이션
description: 혼합 미디어 뷰어가 표시하는 특정 콘텐츠는 현지화가 적용됩니다. 이 지침에는 확대/축소 단추, 스핀 단추, 비디오 컨트롤, 닫기 단추, 전체 화면 단추 및 견본 스크롤 단추가 포함되어 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 119d8dde-145b-4762-a1ab-882a29e0f6a6
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---

# 사용자 인터페이스 요소의 로컬라이제이션{#localization-of-user-interface-elements}

혼합 미디어 뷰어가 표시하는 특정 콘텐츠는 현지화가 적용됩니다. 이 지침에는 확대/축소 단추, 스핀 단추, 비디오 컨트롤, 닫기 단추, 전체 화면 단추 및 견본 스크롤 단추가 포함되어 있습니다.

지역화할 수 있는 뷰어의 모든 텍스트 컨텐츠는 SYMBOL이라는 특수 Viewer SDK 식별자로 표시됩니다. 모든 SYMBOL에는 영어 로케일( `"en"`) 내의 아무 곳에나 사용할 수 있습니다. 또한 필요한 만큼 많은 로케일에 대해 사용자 정의 값을 설정할 수도 있습니다.

뷰어가 시작되면 현재 로케일을 확인하여 로케일에 대해 지원되는 각 SYMBOL에 대해 사용자 정의 값이 있는지 확인합니다. 가 있는 경우 사용자 정의 값을 사용합니다. 그렇지 않으면 기본 텍스트로 돌아갑니다.

사용자 정의 로컬라이제이션 데이터를 로컬라이제이션 JSON 개체로 뷰어에 전달할 수 있습니다. 이러한 객체에는 지원되는 로케일 목록, 각 로케일의 SYMBOL 텍스트 값 및 기본 로캘이 포함되어 있습니다.

이러한 현지화 객체의 예는 다음과 같습니다.

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

위의 예에서 현지화 개체는 두 개의 로케일( `"en"` 및 `"fr"`)을 사용하고 각 로케일에 두 개의 사용자 인터페이스 요소에 대한 지역화를 제공합니다.

웹 페이지 코드는 지역화 개체를 뷰어 생성자에 값으로 전달해야 합니다 `localizedTexts` 구성 객체의 필드입니다. 다른 옵션은 `setLocalizedTexts(localizationInfo)` 메서드를 사용합니다.

지원되는 기호는 다음과 같습니다.

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>기호 </p> </th> 
   <th colname="col2" class="entry"> <p>도구 설명... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>최상위 뷰어 요소에 대한 ARIA 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>기본 보기 구성 요소에 대한 ARIA 역할 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>키보드 사용자에 대한 ARIA 사용 힌트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>기본 보기 구성 요소에 대한 ARIA 역할 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>키보드 사용자에 대한 ARIA 사용 힌트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>기본 보기 구성 요소에 대한 ARIA 역할 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>키보드 사용자에 대한 ARIA 사용 힌트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>닫기 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>확대 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>축소 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>확대/축소 재설정 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>의 데스크탑 시스템 <span class="codeph"> 인라인 </span> 확대/축소 모드. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>의 터치 장치 <span class="codeph"> 인라인 </span> 확대/축소 모드. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>일반 상태의 전체 화면 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>전체 화면 상태의 전체 화면 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>선택한 닫힌 캡션 단추 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>선택하지 않은 닫힌 캡션 단추 상태. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>왼쪽으로 스크롤합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 스크롤 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>위로 스크롤합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>아래로 스크롤합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>왼쪽 회전 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 회전 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>재생 일시 정지 단추 상태를 선택했습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>재생 일시 정지 단추 상태를 선택 취소합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY </span> </p> </td> 
   <td colname="col2"> <p>재생 일시 정지 단추 상태. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>비디오 스크러버. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대의 비디오 시간입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>선택한 가변 볼륨 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>선택 취소된 가변 볼륨. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p>ARIA를 통해 노출되는 볼륨 슬라이더 노브 레이블 <span class="codeph"> aria-valuettext </span> 속성을 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR </span> </p> </td> 
   <td colname="col2"> <p>비디오를 재생할 수 없을 때 표시되는 오류 메시지입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
