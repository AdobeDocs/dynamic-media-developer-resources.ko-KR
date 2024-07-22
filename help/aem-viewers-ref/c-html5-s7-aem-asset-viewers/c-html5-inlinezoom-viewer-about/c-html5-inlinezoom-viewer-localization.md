---
title: 사용자 인터페이스 요소의 현지화
description: 플라이아웃 뷰어가 표시하는 특정 컨텐츠는 현지화가 적용됩니다. 이 콘텐츠에는 로드 시 플라이아웃 확대/축소 보기에 표시되는 사용자 인터페이스 요소 도구 설명 및 정보 메시지가 포함되어 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 49795aa1-07c7-4f2e-bfd9-51d6581898ed
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# 사용자 인터페이스 요소의 현지화{#localization-of-user-interface-elements}

플라이아웃 뷰어가 표시하는 특정 컨텐츠는 현지화가 적용됩니다. 이 콘텐츠에는 로드 시 플라이아웃 확대/축소 보기에 표시되는 사용자 인터페이스 요소 도구 설명 및 정보 메시지가 포함되어 있습니다.

현지화할 수 있는 뷰어의 모든 텍스트 콘텐츠는 SYMBOL이라는 특수한 뷰어 SDK 식별자에 의해 표현됩니다. 모든 SYMBOL에는 기본 뷰어와 함께 제공되는 영어 로케일(`"en"`)에 대한 기본 관련 텍스트 값이 있으며, 필요한 만큼 로케일에 대해 사용자 정의 값이 설정되어 있을 수도 있습니다.

뷰어가 시작되면 현재 로케일을 확인하여 해당 로케일에 대해 지원되는 각 SYMBOL에 대한 사용자 정의 값이 있는지 확인합니다. 있는 경우 사용자 정의 값을 사용하고, 그렇지 않은 경우 기본 텍스트로 돌아갑니다.

사용자 정의 로컬라이제이션 데이터를 로컬라이제이션 JSON 개체로 뷰어에 전달할 수 있습니다. 이러한 객체에는 지원되는 로케일 목록, 각 로케일에 대한 SYMBOL 텍스트 값 및 기본 로케일이 포함됩니다.

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

위의 예에서 현지화 개체는 두 개의 로케일(`"en"` 및 `"fr"`)을 정의하고 각 로케일에서 두 개의 사용자 인터페이스 요소에 대한 현지화를 제공합니다.

웹 페이지 코드는 구성 개체의 `localizedTexts` 필드 값으로 이러한 로컬라이제이션 개체를 뷰어 생성자에 전달해야 합니다. 다른 방법은 `setLocalizedTexts(localizationInfo)` 메서드를 호출하여 현지화 개체를 전달하는 것입니다.

지원되는 기호는 다음과 같습니다.

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
   <td colname="col2"> <p>키보드 사용자에 대한 ARIA 사용 힌트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>데스크탑 시스템에 대한 정보 메시지. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>터치 장치에 대한 정보 메시지. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>왼쪽 스크롤 단추 툴팁입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>오른쪽 스크롤 단추 툴팁 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>위로 스크롤 단추 툴팁입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>아래로 스크롤하기 위한 툴팁입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
