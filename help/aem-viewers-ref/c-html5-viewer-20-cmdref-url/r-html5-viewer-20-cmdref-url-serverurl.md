---
title: serverUrl
description: 모든 뷰어에 공통되는 매개 변수입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
TQID: 'https://experienceleague.adobe.com/SbAeHSjxnw-69wsu92UeoEeGLlk3Ykpechs65I-k5EY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 3%

---

# serverUrl{#serverurl}

모든 뷰어에 공통되는 매개 변수입니다.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>상대 또는 절대 이미지 제공 루트 경로입니다. </p> <p> 뷰어가 이미지를 검색하는 이미지 제공의 상대 또는 절대 경로를 지정합니다. 경로에 선행 <span class="filepath">/</span>이(가) 없으면 뷰어 HTML 페이지의 위치를 기준으로 합니다. 경로에 선행 <span class="filepath">/</span>이(가) 있는 경우 동일한 서버의 절대 경로를 지정합니다. </p> <p> 뷰어에서 이메일 공유 모듈이 활성화된 경우 절대 경로만 사용합니다. </p> </td> 
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

<!--

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

-->
