---
description: 대화형 이미지 뷰어에 표시되는 특정 컨텐트는 로컬라이제이션을 따릅니다. 여기에는 로드 시 플라이아웃 확대/축소 보기에 의해 표시되는 사용자 인터페이스 요소 도구 설명 및 정보 메시지가 포함됩니다.
seo-description: 대화형 이미지 뷰어에 표시되는 특정 컨텐트는 로컬라이제이션을 따릅니다. 여기에는 로드 시 플라이아웃 확대/축소 보기에 의해 표시되는 사용자 인터페이스 요소 도구 설명 및 정보 메시지가 포함됩니다.
seo-title: 사용자 인터페이스 요소의 로컬라이제이션
title: 사용자 인터페이스 요소의 로컬라이제이션
uuid: 1a22570b-8435-4e57-a022-34428bddc7f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---


# 사용자 인터페이스 요소의 현지화{#localization-of-user-interface-elements}

대화형 이미지 뷰어에 표시되는 특정 컨텐트는 로컬라이제이션을 따릅니다. 여기에는 로드 시 플라이아웃 확대/축소 보기에 의해 표시되는 사용자 인터페이스 요소 도구 설명 및 정보 메시지가 포함됩니다.

지역화할 수 있는 뷰어의 모든 텍스트 컨텐츠는 SYMBOL이라는 특수 뷰어 SDK 식별자로 표시됩니다. 모든 SYMBOL은 기본 뷰어와 함께 제공된 영어 로케일( `"en"`)에 대한 기본 관련 텍스트 값을 가지며, 필요에 따라 많은 로캘에 대해 사용자 정의 값을 설정할 수도 있습니다.

뷰어가 시작되면 지원되는 각 SYMBOL에서 해당 로캘에 대해 사용자 정의 값이 있는지 확인하기 위해 현재 로캘을 확인합니다. 있는 경우 사용자 정의 값을 사용합니다.그렇지 않으면 기본 텍스트로 돌아갑니다.

사용자 정의 현지화 데이터는 로컬라이제이션 JSON 개체로서 뷰어에 전달할 수 있습니다. 이러한 객체에는 지원되는 로케일 목록, 각 로케일에 대한 SYMBOL 텍스트 값 및 기본 로캘이 포함되어 있습니다.

이러한 현지화 객체의 예는 다음과 같습니다.

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>최상위 뷰어 요소에 대한 ARIA 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>기본 보기 구성 요소에 대한 ARIA 역할 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>키보드 사용자를 위한 ARIA 사용 힌트 </p> </td> 
  </tr> 
 </tbody> 
</table>

