---
description: eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.
seo-description: eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 19149e38-b9d2-4ecd-a555-92e2960f7ee3
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---


# setContainerId{#setcontainerid}

eCatalog 뷰어에 대한 JavaScript API 참조 사항입니다.

[!DNL ` setContainerId( *`containerId`*)`]

뷰어가 삽입되는 `DOM` 컨테이너(일반적으로 `DIV`)의 ID를 설정합니다. 이 메서드를 호출할 때까지 컨테이너 요소를 만들 필요가 없습니다. 그러나 `init()`이(가) 실행될 때는 컨테이너가 존재해야 합니다. `init()` 이전에 호출해야 합니다.

이 메서드는 뷰어 구성 정보가 `config` JSON 개체와 함께 생성자에 전달될 때 선택 사항입니다.

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

