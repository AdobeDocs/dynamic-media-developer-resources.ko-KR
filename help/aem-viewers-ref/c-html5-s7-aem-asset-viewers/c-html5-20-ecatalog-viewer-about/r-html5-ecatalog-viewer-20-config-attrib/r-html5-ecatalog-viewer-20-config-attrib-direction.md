---
title: 방향
description: 페이지를 기본 보기 및 축소판에 표시하는 방식을 지정합니다. 또한 사용자가 뷰어 사용자 인터페이스와 상호 작용하여 카탈로그 프레임 간에 변경되는 방법을 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7d3df37-3e8b-438f-8b24-035b6982dc14
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 2%

---

# 방향{#direction}

`direction=auto|left|right`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 자동|왼쪽|오른쪽 </span> </p> </td> 
   <td colname="col2"> <p>페이지를 기본 보기 및 축소판에 표시하는 방식을 지정합니다. 또한 사용자가 뷰어 사용자 인터페이스와 상호 작용하여 카탈로그 프레임 간에 변경되는 방법을 지정합니다. </p> <p>When <span class="codeph"> 왼쪽 </span> 이 변수는 초기 페이지에 대해 오른쪽 정렬을 설정하고 마지막 페이지에 대한 왼쪽 정렬을 설정합니다. 개별 페이지 하위 이미지를 왼쪽에서 오른쪽 렌더링 순서로 결합합니다. 또한 카탈로그를 진행하도록 기본 보기를 오른쪽에서 왼쪽 쓰기 슬라이드 애니메이션을 사용하도록 설정합니다(경우에 따라) <span class="codeph"> PageView.parameters </span> 이(가 슬라이드로 설정되어 있음). 마지막으로 축소판은 왼쪽에서 오른쪽 채우기 순서로 설정됩니다. </p> <p>마찬가지로 <span class="codeph"> 오른쪽 </span> 처음 페이지에 대해 왼쪽 맞춤을 설정하고 마지막 페이지에 대해 오른쪽 맞춤을 설정합니다. 오른쪽에서 왼쪽 렌더링 순서에 따라 개별 페이지 하위 이미지가 결합됩니다. 또한 카탈로그를 진행하도록 기본 보기를 왼쪽에서 오른쪽 슬라이드 애니메이션을 사용하도록 설정합니다(경우에 따라) <span class="codeph"> PageView.parameters </span> 이(가 슬라이드로 설정되어 있음). 마지막으로 축소판 보기가 오른쪽에서 왼쪽으로, 위에서 아래로 채워지도록 축소판 순서를 반대로 바꿉니다. </p> <p>When <span class="codeph"> 자동 </span> 이 설정되면 뷰어가 적용됩니다 <span class="codeph"> 오른쪽 </span> 로캘이 로 설정된 경우 모드 <span class="codeph"> ja; </span>그렇지 않으면 <span class="codeph"> 왼쪽 </span> 모드. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-a66ce10d6c0b449883f654e7e0657e2c}

선택 사항입니다.

## 기본값 {#section-2879062cee1d4030b43ba3b19693f4f8}

`auto`

## 예 {#section-798e4fc8dd9b4b059171b41a608a96ce}

`direction=right`
