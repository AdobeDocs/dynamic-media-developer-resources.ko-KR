---
description: 회전판 뷰어에 대한 구성 속성입니다.
seo-description: 회전판 뷰어에 대한 구성 속성입니다.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 80053511-f0e2-49f6-a1db-cd96c7788703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

회전판 뷰어에 대한 구성 속성입니다.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대와 해당 내용을 표시하거나 숨기는 데 사용되는 효과 유형을 지정합니다. </p> <p>즉시 표시/숨기기를 위해 <span class="codeph"> none</span>으로 설정합니다. </p> <p>점진적 페이드 인/아웃 효과를 제공하려면 <span class="codeph"> 페이드</span>로 설정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> 제어 막대에 등록된 마지막 마우스/터치 이벤트와 시간 제어 막대가 숨겨지는 시간(초)을 지정합니다. </p> <p><span class="codeph"> -1</span>으로 설정하면 구성 요소가 자동 숨기기 효과를 트리거하지 않으므로 항상 화면에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 지속 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 페이드 인/아웃 애니메이션의 지속 시간을 초 단위로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다. 이 명령은 컨트롤 막대 자동 숨기기가 비활성화된 터치 장치에서 무시됩니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

