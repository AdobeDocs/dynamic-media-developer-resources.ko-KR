---
title: 키보드 액세스 가능성 및 탐색
description: 기본 확대/축소, eCatalog, eCatalog 검색, 플라이아웃, 인라인 확대/축소, 혼합 미디어, 스핀, 비디오, 확대/축소, 차원(3D), 회전 메뉴, 대화형 이미지, 대화형 비디오 및 Video360 뷰어 인터페이스에 노출된 모든 기능이 키보드로 액세스할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# 키보드 액세스 가능성 및 탐색{#keyboard-accessibility-and-navigation}

기본 확대/축소, eCatalog, eCatalog 검색, 플라이아웃, 인라인 확대/축소, 혼합 미디어, 스핀, 비디오, 확대/축소, 회전, 차원(3D), 대화형 이미지, 대화형 비디오 및 Video360 뷰어 인터페이스에 노출된 모든 기능이 키보드로 액세스할 수 있습니다.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## 키보드 액세스 가능성 및 탐색 {#topic-f5650e9493404e55a3627c8d1366b861}

기본 확대/축소, eCatalog, eCatalog 검색, 플라이아웃, 인라인 확대/축소, 혼합 미디어, 스핀, 비디오, 확대/축소, 회전, 차원(3D), 대화형 이미지, 대화형 비디오 및 Video360 뷰어 인터페이스에 노출된 모든 기능이 키보드로 액세스할 수 있습니다.

최종 사용자는 **[!UICONTROL 탭]** 및 **[!UICONTROL Shift+Tab]** 키 입력. 사용 **[!UICONTROL 탭]** 입력 포커스를 탭 순서의 다음 사용자 인터페이스 요소로 이동합니다. 사용 **[!UICONTROL Shift+Tab]** 입력 포커스를 이전 사용자 인터페이스 요소로 다시 가져옵니다. 초점 순번은 화면의 자연어 사용자 인터페이스 요소 위치를 따르며, 왼쪽에서 오른쪽, 위에서 아래로 이동합니다.

운영 체제 및 웹 브라우저 설정에 따라 입력 포커스가 있는 사용자 인터페이스 요소는 시각적 포커스 표시를 받습니다. 예를 들어, 시각적 표시기는 사용자 인터페이스 요소 주위에 렌더링되는 얇은 테두리일 수 있습니다.

뷰어 CSS에서 이러한 포커스 강조 표시를 비활성화하거나 사용자 지정할 수 있습니다. 이 도움말 시스템의 목차 특정 뷰어 이름(예: 기본 확대/축소 또는 대화형 비디오)에서 **사용자 지정 *뷰어 이름*** >**&#x200B;포커스 강조 표시&#x200B;**.

개별 뷰어 사용자 인터페이스 요소에서 지원하는 키 입력은 대부분의 경우 명확하고 쉽게 검색됩니다.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>작업 </p> </th> 
   <th colname="col2" class="entry"> <p>키 입력 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>단추 구성 요소 활성화 </p> </td> 
   <td colname="col2"> <p>Space 또는 Enter 키를 누릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>확대 또는 축소 </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> 또는 <span class="uicontrol"> - </span>각각 입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>확대/축소 재설정 </p> </td> 
   <td colname="col2"> <p>Esc 키. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>패닝 </p> </td> 
   <td colname="col2"> <p>위쪽, 아래쪽, 왼쪽 또는 오른쪽 화살표 키. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>360도 이미지 회전 </p> </td> 
   <td colname="col2"> <p>이미지가 재설정 상태일 때 화살표 키를 사용합니다. </p> <p>다차원 스핀 세트로 작업할 때 위쪽 또는 아래쪽 화살표 키를 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제품 견본 선택 </p> </td> 
   <td colname="col2"> <p>위쪽, 아래쪽, 왼쪽 또는 오른쪽 화살표 키; Home 또는 End 키 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>제품 견본 활성화 </p> </td> 
   <td colname="col2"> <p>Space 또는 Enter 키를 누릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비디오 및 대화형 비디오, 점진적 되감기 </p> </td> 
   <td colname="col2"> <p>왼쪽 또는 위쪽 화살표 키. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비디오 및 대화형 비디오, 빠른 앞으로 </p> </td> 
   <td colname="col2"> <p>오른쪽 또는 아래쪽 화살표 키. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비디오 및 대화형 비디오에서 시작 또는 끝으로 이동합니다. </p> </td> 
   <td colname="col2"> <p>Home 또는 End 키를 각각 사용합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비디오 및 대화형 비디오에서 포커스가 슬라이더에 있을 때 볼륨 레벨을 제어합니다 </p> </td> 
   <td colname="col2"> <p>위쪽, 아래쪽, 왼쪽 또는 오른쪽 화살표 키; Home 또는 End 키 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비디오 및 대화형 비디오, 가변 볼륨 </p> </td> 
   <td colname="col2"> <p>화살표, Home 및 End 키를 사용하여 슬라이더 부분에 포커스가 있을 때 볼륨 레벨을 제어합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>비디오, 모달 대화 상자가 표시되면 포커스 순번이 대화 상자 컨트롤로만 제한됩니다. </p> </td> 
   <td colname="col2"> <p>대화 상자를 닫으려면 Esc 키를 누릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>회전판, 기본 보기에서 배너 이미지 변경 </p> </td> 
   <td colname="col2"> <p>왼쪽 또는 오른쪽 화살표 키. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>회전판, 핫스팟 선택 및 핫스팟 활성화 </p> </td> 
   <td colname="col2"> <p>핫스팟 선택: 위쪽, 아래쪽, 왼쪽 또는 오른쪽 화살표 키 </p> <p>핫스팟 활성화: Space 또는 Enter 키를 누릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, 기본 보기에서 페이지 이미지 변경 </p> </td> 
   <td colname="col2"> <p> 왼쪽 또는 오른쪽 화살표 키. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, 축소판 선택 </p> </td> 
   <td colname="col2"> <p>화살표 키; Home 및 End 키. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>전자 카탈로그, 견본 활성화 </p> </td> 
   <td colname="col2"> <p>Space 또는 Enter 키를 누릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, 핫 스팟 선택 </p> </td> 
   <td colname="col2"> <p>화살표 키. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, 활성화 </p> </td> 
   <td colname="col2"> <p>Space 또는 Enter 키를 누릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, 드롭다운 구성 요소 활성화 </p> </td> 
   <td colname="col2"> <p> 아래쪽 화살표 키; Space 또는 Enter 키를 누릅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, 포커스가 드롭다운 패널에 있을 때 </p> </td> 
   <td colname="col2"> <p>활성화 전에 화살표 키를 사용하여 패널에서 특정 항목을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog 모달 대화 상자가 표시되면 포커스가 대화 상자 컨트롤로만 제한됩니다. </p> </td> 
   <td colname="col2"> <p>대화 상자를 닫으려면 Esc 키를 누릅니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
