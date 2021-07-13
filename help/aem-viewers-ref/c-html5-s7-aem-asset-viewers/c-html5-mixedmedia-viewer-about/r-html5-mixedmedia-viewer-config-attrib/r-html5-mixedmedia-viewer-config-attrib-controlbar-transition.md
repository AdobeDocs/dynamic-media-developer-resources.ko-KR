---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대와 해당 콘텐츠를 표시하거나 숨기는 데 사용되는 효과 유형을 지정합니다. </p> <p><span class="codeph"> none</span> 을 사용하여 즉시 표시하고 숨깁니다. <span class="codeph"> 페이드</span>를 사용하여 점진적 페이드 인 및 페이드 아웃 효과를 제공합니다. </p> <p>페이드 기능은 Internet Explorer 8에서 지원되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대가 등록하는 마지막 마우스/터치 이벤트와 시간 컨트롤 막대가 숨기는 시간 사이의 시간(초)을 지정합니다. </p> <p> <span class="codeph"> -1</span>로 설정하면 구성 요소는 자동 숨기기 효과를 트리거하지 않고 항상 화면에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간</span> </span> </p> </td> 
   <td colname="col2"> <p>페이드 인 및 페이드 아웃 애니메이션의 지속 시간을 초 단위로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
