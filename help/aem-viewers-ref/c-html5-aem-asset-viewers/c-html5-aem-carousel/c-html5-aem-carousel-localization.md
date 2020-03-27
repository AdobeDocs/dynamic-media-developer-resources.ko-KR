---
description: 회전판 뷰어에 표시되는 특정 컨텐츠는 로컬라이제이션에 적용됩니다. 여기에는 슬라이드 탐색 단추가 포함됩니다.
seo-description: 회전판 뷰어에 표시되는 특정 컨텐츠는 로컬라이제이션에 적용됩니다. 여기에는 슬라이드 탐색 단추가 포함됩니다.
seo-title: 유저 인터페이스 요소의 로컬라이제이션
solution: Experience Manager
title: 유저 인터페이스 요소의 로컬라이제이션
topic: Dynamic media
uuid: 82e4dc72-cc12-4ab5-8370-6270f9a3d45f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 유저 인터페이스 요소의 로컬라이제이션{#localization-of-user-interface-elements}

회전판 뷰어에 표시되는 특정 컨텐츠는 로컬라이제이션에 적용됩니다. 여기에는 슬라이드 탐색 단추가 포함됩니다.

뷰어의 지역화할 수 있는 모든 텍스트 컨텐츠는 SYMBOL이라는 특수 Viewer SDK 식별자로 표시됩니다. 모든 SYMBOL은 기본 제공 뷰어와 함께 제공되는 영어 로케일( `"en"`)에 대한 기본 관련 텍스트 값을 가지며, 필요에 따라 많은 로캘에 대해 사용자 정의 값을 설정할 수도 있습니다.

뷰어가 시작되면 현재 로케일을 확인하여 지원되는 각 SYMBOL에 해당 로케일에 대해 사용자 정의 값이 있는지 확인합니다. 있는 경우 사용자 정의 값을 사용합니다.그렇지 않으면 기본 텍스트로 돌아갑니다.

사용자 정의 현지화 데이터는 뷰어에 현지화 JSON 개체로 전달될 수 있습니다. 이러한 개체에는 지원되는 로케일 목록, 각 로케일의 SYMBOL 텍스트 값 및 기본 로케일이 포함되어 있습니다.

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

위의 예에서 현지화 개체는 두 개의 로케일( `"en"` 및 `"fr"`)을 정의하고 각 로케일에서 두 개의 사용자 인터페이스 요소에 대한 현지화를 제공합니다.

웹 페이지 코드는 구성 개체의 필드 값으로 현지화 개체를 뷰어 생성자에 전달해야 합니다. `localizedTexts` 대체 옵션은 `setLocalizedTexts(localizationInfo)` 메서드를 호출하여 현지화 개체를 전달하는 것입니다.

다음 심볼이 지원됩니다.

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>기호 </p> </th> 
   <th colname="col2" class="entry"> <p>툴 팁 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>선택한 재생 일시 정지 단추 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>선택하지 않은 재생 일시 정지 단추 상태입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> 이전 및 다음 슬라이드 단추에 대한 도구 설명 및 ARIA 레이블입니다. </p> <p>두 개의 교체 토큰을 수락합니다.현재 슬라이드 색인의 <span class="codeph"> $ </span> CURRENT_FRAME$ 및 <span class="codeph"> $TOTAL_FRAMES$ </span> for the total number of slides. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> 최상위 뷰어 요소에 대한 ARIA 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> 기본 보기 구성 요소에 대한 ARIA 역할 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> 키보드 사용자를 위한 ARIA 파섹 </p> </td> 
  </tr> 
 </tbody> 
</table>

