---
description: 방향
solution: Experience Manager
title: 방향
topic: Dynamic media
uuid: 0a30f3b0-64c8-4799-b4f5-fc8996a8b5a4
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 3%

---


# 방향{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p>기본 보기 및 축소판에 페이지가 표시되는 방식을 지정합니다. 또한 사용자가 뷰어 사용자 인터페이스와 상호 작용하여 카탈로그 프레임 간을 변경하는 방법을 지정합니다. </p> <p><span class="codeph"> left </span>을 사용하면 초기 페이지에 대한 오른쪽 정렬이 설정되고 마지막 페이지에 대한 왼쪽 정렬이 설정됩니다. 왼쪽-오른쪽 렌더링 순서에 따라 개별 페이지 하위 이미지를 연결하여 고정시킵니다. 또한 카탈로그를 진행하도록(예: <span class="codeph"> PageView.frametransition </span>이 슬라이드로 설정된 경우) 오른쪽에서 왼쪽으로 슬라이드 애니메이션을 사용하도록 기본 보기를 설정합니다. 마지막으로 축소판은 왼쪽에서 오른쪽으로 칠 순서로 설정됩니다. </p> <p>마찬가지로, <span class="codeph"> 오른쪽 </span>을 사용하면 초기 페이지에 대한 왼쪽 정렬과 마지막 페이지에 대한 오른쪽 정렬이 설정됩니다. 오른쪽에서 왼쪽으로 렌더링하는 순서로 개별 페이지 하위 이미지를 연결하여 고정시킵니다. 또한 카탈로그를 진행하도록(예: <span class="codeph"> PageView.frametransition </span>이 슬라이드로 설정된 경우) 왼쪽에서 오른쪽 슬라이드 애니메이션을 사용하도록 기본 보기를 설정합니다. 마지막으로 축소판 보기가 오른쪽에서 왼쪽으로, 위에서 아래로 채워지도록 축소판 순서를 되돌립니다. </p> <p>로케일이 <span class="codeph"> ja;로 설정된 경우 뷰어는 <span class="codeph"> auto </span>을(를) 설정한 경우 <span class="codeph"> 오른쪽 </span> 모드를 적용합니다.</span>그렇지 않으면 <span class="codeph"> 왼쪽 </span> 모드를 사용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-a66ce10d6c0b449883f654e7e0657e2c}

선택 사항입니다.

## 기본값 {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## 예 {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
