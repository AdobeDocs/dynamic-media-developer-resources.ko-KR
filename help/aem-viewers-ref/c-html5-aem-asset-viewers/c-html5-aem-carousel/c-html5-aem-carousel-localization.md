---
description: Carousel Viewer에서 표시하는 특정 컨텐츠는 로컬라이제이션을 따릅니다. 여기에는 슬라이드 탐색 단추가 포함됩니다.
solution: Experience Manager
title: 사용자 인터페이스 요소의 로컬라이제이션
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# 사용자 인터페이스 요소의 현지화{#localization-of-user-interface-elements}

Carousel Viewer에서 표시하는 특정 컨텐츠는 로컬라이제이션을 따릅니다. 여기에는 슬라이드 탐색 단추가 포함됩니다.

지역화할 수 있는 뷰어의 모든 텍스트 컨텐츠는 SYMBOL이라는 특수 뷰어 SDK 식별자로 표시됩니다. 모든 SYMBOL은 기본 뷰어와 함께 제공된 영어 로케일( `"en"`)에 대한 기본 관련 텍스트 값을 가지며, 필요에 따라 많은 로캘에 대해 사용자 정의 값을 설정할 수도 있습니다.

뷰어가 시작되면 지원되는 각 SYMBOL에서 해당 로캘에 대해 사용자 정의 값이 있는지 확인하기 위해 현재 로캘을 확인합니다. 있는 경우 사용자 정의 값을 사용합니다.그렇지 않으면 기본 텍스트로 돌아갑니다.

사용자 정의 현지화 데이터는 로컬라이제이션 JSON 개체로서 뷰어에 전달할 수 있습니다. 이러한 객체에는 지원되는 로케일 목록, 각 로케일에 대한 SYMBOL 텍스트 값 및 기본 로캘이 포함되어 있습니다.

이러한 현지화 객체의 예는 다음과 같습니다.

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
}, 
defaultLocale:"en" 
}
```

위의 예에서 현지화 객체는 두 로케일( `"en"` 및 `"fr"`)을 정의하고 각 로케일에 있는 두 개의 사용자 인터페이스 요소에 대한 현지화를 제공합니다.

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
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>선택한 재생 일시 정지 단추 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>선택하지 않은 재생 일시 정지 단추 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO  </span> </p> </td> 
   <td colname="col2"> <p> 이전 및 다음 슬라이드 단추에 대한 도구 설명 및 ARIA 레이블. </p> <p>2개의 교체 토큰을 허용합니다.현재 슬라이드 색인의 경우 <span class="codeph"> $CURRENT_FRAME$ </span>, 총 슬라이드 수의 경우 <span class="codeph"> $TOTAL_FRAMES$ </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p> 최상위 뷰어 요소에 대한 ARIA 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기 구성 요소에 대한 ARIA 역할 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p> 키보드 사용자를 위한 ARIA 사용 힌트 </p> </td> 
  </tr> 
 </tbody> 
</table>
