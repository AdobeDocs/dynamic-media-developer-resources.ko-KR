---
title: contentUrl
description: 모든 뷰어에 공통되는 매개 변수.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 4%

---

# contentUrl{#contenturl}

모든 뷰어에 공통되는 매개 변수.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>사용자 지정 CSS 파일, 자막 컨텐츠 또는 탐색 컨텐츠에 대한 기본 경로를 지정합니다. </p> <p>경로에 선행 <span class="filepath"> /</span>이 없는 경우 이 경로는 뷰어 HTML 페이지의 위치를 기준으로 합니다. 경로에 선행 <span class="filepath"> /</span>이 있는 경우 동일한 서버에 절대 경로를 지정합니다. </p> <p> 스타일 명령을 지정하지 않은 경우 기본 CSS 파일 로드에 영향을 주지 않습니다. </p> </td> 
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
