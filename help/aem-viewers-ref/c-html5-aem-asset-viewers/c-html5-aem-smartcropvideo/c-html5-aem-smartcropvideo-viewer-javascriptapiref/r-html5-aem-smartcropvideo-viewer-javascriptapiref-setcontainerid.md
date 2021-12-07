---
title: setContainerId
description: 스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조.

` setContainerId( *`containerId`*)`

DOM 컨테이너의 ID(일반적으로 `DIV`) 뷰어가 삽입되는 위치에 포함될 수 있습니다. 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요가 없습니다. 그러나 이 컨테이너는 `init()` 가 실행됩니다. 이 매개 변수는 전에 호출됩니다 `init()`. 이 메서드는 뷰어 구성 정보가 `config` 생성자에 대한 JSON 개체.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 컨테이너 ID입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
