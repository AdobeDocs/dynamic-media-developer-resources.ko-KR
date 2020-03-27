---
description: 비디오 이미지 뷰어용 JavaScript API 참조.
seo-description: 비디오 이미지 뷰어용 JavaScript API 참조.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: f1486f82-28dd-4321-a0e5-9e5696f6bbf7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setContainerId{#setcontainerid}

비디오 이미지 뷰어용 JavaScript API 참조.

` setContainerId( *`containerId`*)`

뷰어가 삽입되는 DOM 컨테이너(일반적으로 DIV)의 ID를 설정합니다. 이 메서드를 호출할 때까지 컨테이너 요소를 만들 필요는 없습니다. 그러나 컨테이너는 실행될 때 존재해야 `init()` 합니다. 그 전에 전화해야 `init()`합니다.

이 메서드는 뷰어 구성 정보가 JSON 개체와 함께 생성자에 전달되면 `config` 선택 사항입니다.

## 매개 변수 {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 컨테이너 <span class="varname"> ID </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 컨테이너의 ID입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

