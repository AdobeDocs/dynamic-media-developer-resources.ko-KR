---
title: setParams
description: 파노라마 뷰어에 대한 JavaScript API 참조.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 3%

---

# setParams{#setparams}

파노라마 뷰어에 대한 JavaScript API 참조.

` setParams( *`매개 변수`*)`

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, 다음과 같이 구분된 name=value 쌍을 나타냅니다. `&`. 쿼리 문자열에서와 같이, 이름과 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. 통화하기 전에 `init()`, 이 매개 변수를 호출해야 합니다.

뷰어 구성 정보가 로 전달된 경우 이 메서드는 선택 사항입니다 `config` 생성자에 대한 JSON 개체입니다.


## 매개 변수 {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 매개 변수</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> 다음으로 구분된 name=value 매개 변수 쌍 <span class="codeph"> 및</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PanoramicView.fmt=png&PanoramicView.iscommand=op_sharpen%3d1")
```
