---
title: setContainerId
description: eCatalog Viewer에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 32e75d36-cc9a-42df-95e8-5b48456296e9
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

eCatalog Viewer에 대한 JavaScript API 참조.

` setContainerId( *`containerId`*)`

의 ID를 설정합니다. `DOM` 컨테이너(일반적으로 `DIV`) 내의 아무 곳에나 삽입할 수 있습니다. 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요가 없습니다. 그러나 이 컨테이너는 `init()` 가 실행됩니다. 전에 호출해야 합니다. `init()`.

이 메서드는 뷰어 구성 정보가 `config` 생성자에 대한 JSON 개체.

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
