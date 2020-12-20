---
description: 회전판 뷰어에 대한 JavaScript API 참조입니다.
seo-description: 회전판 뷰어에 대한 JavaScript API 참조입니다.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 3e26c121-7493-49b5-af25-ebd76477a415
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---


# setContainerId{#setcontainerid}

회전판 뷰어에 대한 JavaScript API 참조입니다.

` setContainerId( *`containerId`*)`

뷰어가 삽입되는 DOM 컨테이너(일반적으로 `DIV`)의 ID를 설정합니다. 이 메서드를 호출할 때까지 컨테이너 요소를 만들 필요가 없습니다. 그러나 `init()`이(가) 실행될 때는 컨테이너가 존재해야 합니다. `init()` 이전에 호출해야 합니다.

이 메서드는 뷰어 구성 정보가 `config` JSON 개체와 함께 생성자에 전달될 때 선택 사항입니다.

## 매개 변수 {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 컨테이너의 {string}  </span> ID. </p> </td> 
  </tr> 
 </tbody> 
</table>

## {#section-1d3cf85bc7cc4dfe9670e038d02b9101} 반환

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

