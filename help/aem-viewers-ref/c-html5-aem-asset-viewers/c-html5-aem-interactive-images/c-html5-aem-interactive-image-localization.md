---
title: 사용자 인터페이스 요소의 현지화
description: 대화형 이미지 뷰어가 표시하는 특정 컨텐츠는 현지화가 적용됩니다. 이 콘텐츠에는 사용자 인터페이스 요소 도구 설명과 로드 시 플라이아웃 확대/축소 보기에 표시되는 정보 메시지가 포함되어 있습니다.
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# 사용자 인터페이스 요소의 현지화{#localization-of-user-interface-elements}

대화형 이미지 뷰어가 표시하는 특정 컨텐츠는 현지화가 적용됩니다. 이 콘텐츠에는 사용자 인터페이스 요소 도구 설명과 로드 시 플라이아웃 확대/축소 보기에 표시되는 정보 메시지가 포함되어 있습니다.

현지화할 수 있는 뷰어의 모든 텍스트 콘텐츠는 SYMBOL이라는 특수한 뷰어 SDK 식별자에 의해 표현됩니다. 모든 SYMBOL에는 영어 로케일에 대한 기본 연관 텍스트 값이 있습니다( `"en"`)는 기본 뷰어와 함께 제공되며, 필요한 만큼 많은 로케일에 대해 사용자 정의 값이 설정될 수 있습니다.

뷰어가 시작되면 현재 로케일을 확인하여 해당 로케일에 대해 지원되는 각 SYMBOL에 대한 사용자 정의 값이 있는지 확인합니다. 있는 경우 사용자 정의 값을 사용하고, 그렇지 않은 경우 기본 텍스트로 돌아갑니다.

사용자 정의 로컬라이제이션 데이터를 로컬라이제이션 JSON 개체로 뷰어에 전달할 수 있습니다. 이러한 객체에는 지원되는 로케일 목록, 각 로케일에 대한 SYMBOL 텍스트 값 및 기본 로케일이 포함됩니다.

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
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>기본 보기 구성 요소에 대한 ARIA 역할 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>키보드 사용자에 대한 ARIA 사용 힌트입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
