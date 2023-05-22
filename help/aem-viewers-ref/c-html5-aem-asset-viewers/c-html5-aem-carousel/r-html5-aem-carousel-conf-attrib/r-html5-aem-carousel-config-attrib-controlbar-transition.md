---
title: ControlBar.transition
description: 슬라이드 뷰어에 대한 구성 속성입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

슬라이드 뷰어에 대한 구성 속성입니다.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`지연 숨기기`*[, *`지속 시간`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 없음|페이드</span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대 및 해당 내용을 표시하거나 숨기는 데 사용할 효과 유형을 지정합니다. </p> <p>다음으로 설정 <span class="codeph"> 없음</span> 즉시 표시하거나 숨길 수 있습니다. </p> <p>다음으로 설정 <span class="codeph"> 페이드</span> 점진적인 페이드 인/아웃 효과를 제공합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 지연 숨기기</span></span> </p> </td> 
   <td colname="col2"> <p> 컨트롤 막대에 등록된 마지막 마우스/터치 이벤트와 시간 컨트롤 막대가 숨기는 간격(초)을 지정합니다. </p> <p>로 설정된 경우 <span class="codeph"> -1</span> 구성 요소가 자동 숨기기 효과를 트리거하지 않으므로 항상 화면에 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 지속 시간</span></span> </p> </td> 
   <td colname="col2"> <p> 페이드 인/아웃 애니메이션의 지속 시간(초)을 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-1e637b22e8a44d759d588e47576891e6}

선택적. 이 명령은 컨트롤 막대 자동 숨기기가 비활성화된 터치 장치에서는 무시됩니다.

## 기본값 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 예 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
