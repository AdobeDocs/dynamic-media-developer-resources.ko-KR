---
title: 사용자 인터페이스 요소의 로컬라이제이션
description: eCatalog Viewer에 표시되는 특정 컨텐츠는 확대/축소 단추, 페이지 변경 단추, 축소판 단추, 전체 화면 단추, 닫기 단추 및 스크롤 막대 단추 등 로컬라이제이션의 적용을 받습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 1d7e9eba-b30c-4f85-b551-6842f73dc22c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 0%

---

# 사용자 인터페이스 요소의 로컬라이제이션{#localization-of-user-interface-elements}

eCatalog Viewer에 표시되는 특정 컨텐츠는 확대/축소 단추, 페이지 변경 단추, 축소판 단추, 전체 화면 단추, 닫기 단추 및 스크롤 막대 단추 등 로컬라이제이션의 적용을 받습니다.

지역화할 수 있는 뷰어의 모든 텍스트 컨텐츠는 SYMBOL이라는 특수 Viewer SDK 식별자로 표시됩니다. 모든 SYMBOL에는 영어 로케일( `"en"`) 즉시 사용 가능한 뷰어와 함께 제공될 수 있고, 필요에 따라 많은 로케일에 대해 사용자 정의 값을 설정할 수도 있습니다.

뷰어가 시작되면 현재 로케일을 확인하여 로케일에 지원되는 각 SYMBOL에 대해 사용자 정의 값이 있는지 확인합니다. 가 있는 경우 사용자 정의 값을 사용합니다. 그렇지 않으면 기본 텍스트로 돌아갑니다.

사용자 정의 로컬라이제이션 데이터를 로컬라이제이션 JSON 개체로 뷰어에 전달할 수 있습니다. 이러한 객체에는 지원되는 로케일 목록, 각 로케일의 SYMBOL 텍스트 값 및 기본 로캘이 포함되어 있습니다.

이러한 현지화 객체의 예:

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

웹 페이지 코드는 이러한 지역화 개체를 뷰어 생성자에 값으로 전달해야 합니다. `localizedTexts` 구성 객체의 필드입니다. 다른 옵션은 를 호출하여 현지화 개체를 전달하는 것입니다 `setLocalizedTexts(localizationInfo)` 메서드를 사용합니다.

다음 기호가 지원됩니다(containerId가 뷰어 컨테이너의 ID라고 가정).

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
   <td colname="col1"> <p> <span class="codeph"> PageView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>기본 보기 구성 요소에 대한 ARIA 역할 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.USAGE_HINT </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>일반 상태의 전체 화면 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>전체 화면 상태의 전체 화면 단추. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_rightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>큰 다음 페이지 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_leftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>큰 이전 페이지 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_lastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>마지막 페이지 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_secondaryLastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>마지막 페이지 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_firstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>첫 번째 페이지 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_secondaryFirstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>첫 번째 페이지 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_toolBarRightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>다음 페이지 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerid&gt;_toolBarLeftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>이전 페이지 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>축소판 모드의 축소판 그림 단추 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>일반 모드의 축소판 단추 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>닫기 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InfoPanelPopup.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>정보 패널 닫기 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>소셜 공유 도구. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>전자 메일 공유 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>이메일 대화 상자 헤더. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>전자 메일 대화 상자의 오른쪽 상단 닫기 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESSES </span> </p> </td> 
   <td colname="col2"> <p>전자 메일 주소의 형식이 잘못된 경우 표시되는 오류 메시지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO </span> </p> </td> 
   <td colname="col2"> <p>받는 사람 입력 필드에 대한 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>다른 이메일 주소 추가 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD </span> </p> </td> 
   <td colname="col2"> <p>다른 이메일 주소 추가 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM </span> </p> </td> 
   <td colname="col2"> <p>입력 필드에서. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE </span> </p> </td> 
   <td colname="col2"> <p>메시지 입력 필드. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE </span> </p> </td> 
   <td colname="col2"> <p>이메일 주소 제거 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>취소 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>취소 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>모두 선택 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>모두 선택 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE </span> </p> </td> 
   <td colname="col2"> <p>양식을 제출한 후 대화 상자 하단에 표시되는 닫기 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>양식을 제출한 후 대화 상자 하단에 표시되는 닫기 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>양식 제출 단추에 대한 캡션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>양식 제출 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS </span> </p> </td> 
   <td colname="col2"> <p>전자 메일을 성공적으로 보냈을 때 확인 메시지가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE </span> </p> </td> 
   <td colname="col2"> <p>이메일을 성공적으로 보내지 못할 때 표시되는 오류 메시지입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>포함 공유 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>포함 대화 상자 헤더. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>포함 대화 상자의 오른쪽 상단 닫기 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>포함 코드 텍스트에 대한 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>포함 크기 콤보 상자의 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>취소 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>취소 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>포함 크기 콤보 상자의 마지막 "사용자 지정 크기" 항목에 대한 텍스트입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>링크 공유 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>링크 대화 상자 헤더입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>링크 대화 상자의 오른쪽 상단 닫기 단추입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>공유 링크에 대한 설명입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>취소 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>취소 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>모두 선택 단추에 대한 캡션입니다. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>인쇄 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.HEADER </span> </p> </td> 
   <td colname="col2"> <p>대화 상자 헤더 인쇄 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>인쇄 대화 상자 오른쪽 상단의 닫기 단추 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE </span> </p> </td> 
   <td colname="col2"> <p>"인쇄 페이지 선택" 섹션의 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_CURRENT </span> </p> </td> 
   <td colname="col2"> <p>"현재 페이지" 라디오 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_FROM </span> </p> </td> 
   <td colname="col2"> <p>"다음에서 범위 확산" 라디오 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_TO </span> </p> </td> 
   <td colname="col2"> <p>끝 숫자 선택기의 캡션. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_ALL </span> </p> </td> 
   <td colname="col2"> <p>모든 페이지 라디오 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING </span> </p> </td> 
   <td colname="col2"> <p>"페이지 처리" 섹션의 레이블입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_ONE </span> </p> </td> 
   <td colname="col2"> <p>"시트당 1페이지" 라디오 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_TWO </span> </p> </td> 
   <td colname="col2"> <p>"시트당 2페이지" 라디오 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>취소 단추에 대한 캡션입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p> 취소 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.ACTION </span> </p> </td> 
   <td colname="col2"> <p>인쇄로 보내기 단추에 대한 캡션 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> 인쇄로 보내기 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 즐겨찾기 메뉴.도구 설명 </span> </p> </td> 
   <td colname="col2"> <p>즐겨찾기 메뉴 단추. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>즐겨찾기 편집 모드에서 "즐겨찾기 추가" 단추를 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>일반 모드에서 "즐겨찾기 추가" 단추를 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>즐겨찾기 편집 모드에서 "즐겨찾기 제거" 단추 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>일반 모드에서 "즐겨찾기 제거" 단추를 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 보기AllFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>즐겨찾기 보기가 활성 상태일 때 "모든 즐겨찾기 보기" 단추를 클릭합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 보기AllFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>즐겨찾기 보기가 비활성화되어 있으면 "모든 즐겨찾기 보기" 단추가 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 즐겨찾기 효과.도구 설명 </span> </p> </td> 
   <td colname="col2"> <p>단일 즐겨찾기 아이콘. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_XX[_YY] </span> </p> </td> 
   <td colname="col2"> <p>로드 시 뷰어가 생성하는 페이지 레이블입니다. </p> <p>해당 기호의 이름은 템플릿입니다. 여기서 <span class="codeph"> XX </span> 가로 방향의 0기반 확산 색인이며, 선택 사항입니다 <span class="codeph"> YY </span> 는 대상 스프레드 내의 0기반 페이지 색인입니다. <span class="codeph"> XX </span>. </p> <p>처음 로드된 자산에 대해서만 적용됩니다. 자산을 <span class="codeph"> setAsset() </span> API 호출. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_DELIM </span> </p> </td> 
   <td colname="col2"> <p> 스프레드 내의 왼쪽 및 오른쪽 페이지에 대해 레이블이 정의될 경우 페이지 레이블 구분 기호로 사용되는 문자입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 막대에서 왼쪽으로 스크롤합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>기본 컨트롤 모음 오른쪽 스크롤 단추. </p> </td> 
  </tr> 
 </tbody> 
</table>
