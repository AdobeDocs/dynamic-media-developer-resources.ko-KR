---
title: serverUrl
description: 모든 뷰어에 공통되는 매개 변수입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# serverUrl{#serverurl}

모든 뷰어에 공통되는 매개 변수입니다.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>상대 또는 절대 이미지 제공 루트 경로입니다. </p> <p> 뷰어가 이미지를 검색하는 이미지 제공의 상대 또는 절대 경로를 지정합니다. 패스에 행간이 없는 경우 <span class="filepath"> /</span>: 뷰어 HTML 페이지의 위치를 기준으로 합니다. 패스에 행간이 있는 경우 <span class="filepath"> /</span>, 동일한 서버의 절대 경로를 지정합니다. </p> <p> 뷰어에서 이메일 공유 모듈이 활성화된 경우 절대 경로만 사용합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-10ee45d637134e0fbcd943c62578cb78}

선택적. 표준 SaaS(Software as a Service) 사용에는 필요하지 않습니다.

## 기본값 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## 예제 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```
