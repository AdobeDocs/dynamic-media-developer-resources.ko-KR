---
title: setContainerId
description: 혼합 미디어 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: b6e191dc-3172-45ba-b6f6-258cfbd5855d
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

혼합 미디어 뷰어에 대한 JavaScript API 참조입니다.

` setContainerId( *`containerId`*)`

뷰어가 삽입되는 DOM 컨테이너(일반적으로 DIV)의 ID를 설정합니다. 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요는 없습니다. 단, 컨테이너는 다음과 같은 경우에 존재해야 합니다. `init()` 가 실행되었습니다. 전에 호출해야 합니다. `init()`. 뷰어 구성 정보가 로 전달되는 경우 이 메서드는 선택 사항입니다. `config` 생성자에 대한 JSON 개체입니다.

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
