---
description: 널
seo-description: 널
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 803df8d4-6fb9-49ef-a097-c883d4115fad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대와 해당 컨텐츠를 표시하거나 숨기는 데 사용되는 효과 유형을 지정합니다. </p> <p>아무 <span class="codeph"> 것도</span> 즉시 표시하거나 숨길 수 있습니다. 페이드를 <span class="codeph"></span> 사용하여 점진적인 페이드 인 및 페이드 아웃 효과를 제공할 수 있습니다. </p> <p>Internet Explorer 8에서는 페이드가 지원되지 않습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p>컨트롤 막대가 등록하는 마지막 마우스/터치 이벤트와 시간 컨트롤 막대가 숨기는 시간 사이의 시간(초)을 지정합니다. </p> <p> -1 <span class="codeph"> 로</span> 설정하면 구성 요소가 자동 숨기기 효과를 트리거하지 않고 항상 화면에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 기간</span></span> </p> </td> 
   <td colname="col2"> <p>페이드 인 및 페이드 아웃 애니메이션의 지속 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
