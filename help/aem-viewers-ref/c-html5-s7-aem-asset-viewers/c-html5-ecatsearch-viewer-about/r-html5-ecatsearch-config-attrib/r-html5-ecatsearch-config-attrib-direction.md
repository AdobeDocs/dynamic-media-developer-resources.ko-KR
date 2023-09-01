---
title: 방향
description: 방향
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0f78a835-9057-4c79-843a-52b33a1bdd3f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---

# 방향{#direction}

[!DNL `direction=auto|left|right`]

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|왼쪽|오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>페이지가 기본 보기 및 썸네일에 표시되는 방식을 지정합니다. 또한 사용자가 뷰어 사용자 인터페이스와 상호 작용하여 카탈로그 프레임 사이를 변경하는 방식을 지정합니다. </p> <p>날짜 <span class="codeph"> left </span> 초기 페이지에 대한 오른쪽 맞춤과 마지막 페이지에 대한 왼쪽 맞춤을 설정하는 데 사용됩니다. 왼쪽에서 오른쪽 렌더링 순서를 위해 개별 페이지 하위 이미지를 결합합니다. 또한 오른쪽에서 왼쪽 슬라이드 애니메이션을 사용하여 카탈로그를 진행하도록 기본 보기를 설정합니다(이 경우 <span class="codeph"> PageView.frametransition </span> 가 slide)로 설정되어 있습니다. 마지막으로, 축소판은 왼쪽에서 오른쪽으로 채우도록 설정됩니다. </p> <p>마찬가지로 다음과 같은 경우: <span class="codeph"> 오른쪽 </span> 초기 페이지에 대한 왼쪽 맞춤과 마지막 페이지에 대한 오른쪽 맞춤을 설정하는 데 사용됩니다. 오른쪽에서 왼쪽 렌더링 순서를 위해 개별 페이지 하위 이미지를 결합합니다. 또한 왼쪽-오른쪽 슬라이드 애니메이션을 사용하여 카탈로그를 진행하도록 기본 보기를 설정합니다(이 경우 <span class="codeph"> PageView.frametransition </span> 가 slide)로 설정되어 있습니다. 마지막으로 축소판 보기를 오른쪽에서 왼쪽, 위에서 아래로 채우도록 축소판 순서를 반대로 합니다. </p> <p>날짜 <span class="codeph"> auto </span> 이 설정되면 뷰어가 적용됩니다. <span class="codeph"> 오른쪽 </span> locale이 로 설정된 경우 모드 <span class="codeph"> ja; </span>그렇지 않으면 <span class="codeph"> left </span> 모드. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-a66ce10d6c0b449883f654e7e0657e2c}

선택적.

## 기본값 {#section-2879062cee1d4030b43ba3b19693f4f8}

[!DNL `auto`]

## 예 {#section-798e4fc8dd9b4b059171b41a608a96ce}

[!DNL `direction=right`]
