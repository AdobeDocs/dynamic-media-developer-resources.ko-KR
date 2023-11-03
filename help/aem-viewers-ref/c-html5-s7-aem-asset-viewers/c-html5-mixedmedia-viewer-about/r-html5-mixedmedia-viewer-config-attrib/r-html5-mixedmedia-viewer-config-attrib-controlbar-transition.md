---
title: ControlBar.transition
description: ControlBar.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`지연 숨기기`*[, *`지속 시간`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대 및 해당 내용을 표시하거나 숨기는 데 사용할 효과 유형을 지정합니다. </p> <p>사용 <span class="codeph"> 없음</span> 즉시 표시하거나 숨길 수 있습니다. 사용 <span class="codeph"> 페이드</span> 를 사용하여 점진적인 페이드 인/페이드 아웃 효과를 제공할 수 있습니다. </p> <p>페이드는 Internet Explorer 8에서 지원되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지연 숨기기</span> </span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대가 등록한 마지막 마우스/터치 이벤트와 컨트롤 막대가 숨기는 시간(초)을 지정합니다. </p> <p> 로 설정된 경우 <span class="codeph"> -1</span>, 구성 요소가 자동 숨기기 효과를 트리거하지 않고 항상 화면에서 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 지속 시간</span> </span> </p> </td> 
   <td colname="col2"> <p>페이드 인 및 페이드 아웃 애니메이션의 지속 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택적.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
