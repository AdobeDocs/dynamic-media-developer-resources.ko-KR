---
title: setContainerId
description: 플라이아웃 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 5e07cbba-c1c1-4c85-af2b-ab2d84fbb709
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

플라이아웃 뷰어에 대한 JavaScript API 참조.

` setContainerId( *`containerId`*)`

DOM 컨테이너의 ID를 설정합니다(일반적으로 `DIV`)을 클릭하여 뷰어를 삽입합니다. 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요는 없습니다. 단, 컨테이너는 다음과 같은 경우에 존재해야 합니다. `init()` 가 실행되었습니다. 전에 호출해야 합니다. `init()`. 뷰어 구성 정보가 로 전달되는 경우 이 메서드는 선택 사항입니다. `config` 생성자에 대한 JSON 개체입니다.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 컨테이너 ID. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
