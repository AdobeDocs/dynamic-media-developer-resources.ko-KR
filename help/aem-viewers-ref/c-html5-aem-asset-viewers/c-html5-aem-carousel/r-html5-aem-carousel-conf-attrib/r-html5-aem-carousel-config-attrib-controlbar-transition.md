---
title: ControlBar.transition
description: 회전판 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# ControlBar.transition{#controlbar-transition}

회전판 뷰어에 대한 구성 속성입니다.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대와 해당 콘텐츠를 표시하거나 숨기는 데 사용되는 효과 유형을 지정합니다. </p> <p>즉시 표시/숨기려면 <span class="codeph"> none</span>으로 설정합니다. </p> <p>점진적 페이드 인/아웃 효과를 제공하려면 <span class="codeph"> 페이드</span>로 설정하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대에서 등록한 마지막 마우스/터치 이벤트와 시간 컨트롤 막대가 숨기는 사이의 시간(초)을 지정합니다. </p> <p><span class="codeph"> -1</span>로 설정하면 구성 요소가 자동 숨기기 효과를 트리거하지 않으므로 항상 화면에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 지속 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 페이드 인/아웃 애니메이션의 지속 시간을 초 단위로 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택 사항입니다. 이 명령은 컨트롤 막대 자동 숨김을 사용하지 않도록 설정한 터치 장치에서 무시됩니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
