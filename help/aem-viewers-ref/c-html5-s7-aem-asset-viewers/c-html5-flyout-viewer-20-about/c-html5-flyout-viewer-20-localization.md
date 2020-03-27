---
description: 플라이아웃 뷰어가 표시하는 특정 컨텐츠는 현지화의 적용을 받습니다. 이 컨텐츠에는 로드 시 플라이아웃 확대/축소 보기로 표시되는 사용자 인터페이스 요소 도구 팁과 정보 메시지가 포함됩니다.
seo-description: 플라이아웃 뷰어가 표시하는 특정 컨텐츠는 현지화의 적용을 받습니다. 이 컨텐츠에는 로드 시 플라이아웃 확대/축소 보기로 표시되는 사용자 인터페이스 요소 도구 팁과 정보 메시지가 포함됩니다.
seo-title: 유저 인터페이스 요소의 로컬라이제이션
solution: Experience Manager
title: 유저 인터페이스 요소의 로컬라이제이션
topic: Dynamic media
uuid: efba09ad-200b-4540-8876-c9e462ec233a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 유저 인터페이스 요소의 로컬라이제이션{#localization-of-user-interface-elements}

플라이아웃 뷰어가 표시하는 특정 컨텐츠는 현지화의 적용을 받습니다. 이 컨텐츠에는 로드 시 플라이아웃 확대/축소 보기로 표시되는 사용자 인터페이스 요소 도구 팁과 정보 메시지가 포함됩니다.

뷰어의 지역화할 수 있는 모든 텍스트 컨텐츠는 SYMBOL이라는 특수 Viewer SDK 식별자로 표시됩니다. 모든 SYMBOL에는 기본 제공 뷰어와 함께 제공되는 영어 로케일( `"en"`)에 대한 기본 관련 텍스트 값이 있습니다. 또한 필요에 따라 많은 로캘에 대해 사용자 정의 값이 설정될 수 있습니다.

뷰어가 시작되면 현재 로케일을 확인하여 로케일에 대해 지원되는 각 SYMBOL에 대해 사용자 정의 값이 있는지 확인합니다. 있는 경우 사용자 정의 값을 사용합니다.그렇지 않으면 기본 텍스트로 돌아갑니다.

사용자 정의 현지화 데이터는 뷰어에 현지화 JSON 개체로 전달될 수 있습니다. 이러한 개체에는 지원되는 로케일 목록, 각 로케일의 SYMBOL 텍스트 값 및 기본 로케일이 포함되어 있습니다.

이러한 현지화 객체의 예는 다음과 같습니다.

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

위의 예에서 현지화 개체는 두 개의 로케일( `"en"` 및 `"fr"`)을 정의하고 각 로케일에서 두 개의 사용자 인터페이스 요소에 대한 현지화를 제공합니다.

웹 페이지 코드는 구성 개체의 `localizedTexts` 필드 값으로 현지화 개체를 뷰어 생성자에 전달해야 합니다. 대체 옵션은 `setLocalizedTexts(localizationInfo)` 메서드를 호출하여 현지화 개체를 전달하는 것입니다.

다음 심볼이 지원됩니다.

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>기호 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>최상위 뷰어 요소에 대한 ARIA 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>기본 보기 구성 요소에 대한 ARIA 역할 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>키보드 사용자를 위한 ARIA 파섹 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>데스크탑 시스템을 위한 정보 메시지 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>터치 장치용 정보 메시지 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>왼쪽 스크롤 단추에 대한 도구 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 스크롤 단추에 대한 도구 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>위로 스크롤하기 위한 툴팁입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>아래로 스크롤하기 위한 툴팁입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

