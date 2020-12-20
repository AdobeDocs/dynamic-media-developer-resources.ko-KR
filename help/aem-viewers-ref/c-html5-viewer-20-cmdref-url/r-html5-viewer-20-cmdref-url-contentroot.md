---
description: 모든 뷰어에 공통되는 매개 변수입니다.
seo-description: 모든 뷰어에 공통되는 매개 변수입니다.
seo-title: contentUrl
solution: Experience Manager
title: contentUrl
topic: Dynamic media
uuid: 85b00c4e-b382-4970-b780-e4ef59108cb7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# contentUrl{#contenturl}

모든 뷰어에 공통되는 매개 변수입니다.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>사용자 지정 CSS 파일, 모든 폐쇄형 캡션 컨텐츠 또는 탐색 컨텐츠의 기본 경로를 지정합니다. </p> <p>경로에 선행 <span class="filepath"> /</span>이 없는 경우, 이 경로는 뷰어 HTML 페이지의 위치를 기준으로 합니다. 경로에 선행 <span class="filepath"> /</span>이 있는 경우 동일한 서버에 대한 절대 경로를 지정합니다. </p> <p> 스타일 명령을 지정하지 않을 때 기본 CSS 파일 로딩에 영향을 주지 않습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-10ee45d637134e0fbcd943c62578cb78}

선택 사항입니다.

## 기본값 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 예제 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```

