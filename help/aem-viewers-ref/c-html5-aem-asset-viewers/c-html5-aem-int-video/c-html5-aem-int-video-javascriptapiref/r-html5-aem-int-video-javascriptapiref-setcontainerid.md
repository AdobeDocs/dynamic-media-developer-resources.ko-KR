---
title: setContainerId
description: 대화형 비디오 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 47fbfd39-a1f4-4deb-b064-306ca9fd3ae7
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

대화형 비디오 뷰어에 대한 JavaScript API 참조입니다.

` setContainerId( *`containerId`*)`

뷰어가 삽입되는 DOM 컨테이너(일반적으로 DIV)의 ID를 설정합니다. 이 메서드가 호출될 때까지 컨테이너 요소를 만들 필요는 없습니다. 단, 컨테이너는 다음과 같은 경우에 존재해야 합니다. `init()` 가 실행되었습니다. 전에 호출해야 합니다. `init()`.

이 메서드는 뷰어 구성 정보가 `config` 생성자에 대한 JSON 개체입니다.

## 매개 변수 {#section-fa807db629ce43bab286b1e1dc96c492}

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
