---
title: setParam
description: 파노라마 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# setParam{#setparam}

파노라마 뷰어에 대한 JavaScript API 참조.

` setParam( *`이름, 값`*)`

viewer 매개 변수를 지정된 값으로 설정합니다. 매개 변수는 뷰어별 구성 옵션 또는 소프트웨어 개발 키트 수정자입니다. 이 매개 변수는 `init()` 전에 호출됩니다.

뷰어 구성 정보가 `config` JSON 개체와 함께 생성자에 전달된 경우 이 메서드는 선택 사항입니다.



<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 이름 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> 매개 변수 이름. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 값 </span> </span> </p> </td> 
   <td colname="col2"> <p> 매개 변수의 <span class="codeph"> {string} </span> 값입니다. 값은 퍼센트 인코딩할 수 없습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
