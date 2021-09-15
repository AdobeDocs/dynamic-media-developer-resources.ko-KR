---
title: initialFrame
description: 모든 뷰어에 공통되는 매개 변수.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# initialFrame{#initialframe}

모든 뷰어에 공통되는 매개 변수.

>[!NOTE]
>
>이 명령은 비디오 이미지 뷰어에는 적용되지 않습니다.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> 뷰어가 로드 시 표시되는 0기반 프레임 인덱스를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>장치가 세로 방향일 때 스프레드 내에 있는 페이지의 인덱스(0부터 시작)입니다. "왼쪽에서 오른쪽" 환경의 경우 <span class="codeph"> 0</span>은 "left page"를 의미하고 <span class="codeph"> 1</span>은 "right page"를 의미합니다. "오른쪽에서 왼쪽" 환경의 경우 반대입니다. <span class="codeph"> 0</span>은 "오른쪽 페이지"를 의미하고 <span class="codeph"> 1</span>은 "left page"를 의미합니다. </p> <p>지정하지 않으면 기본적으로 <span class="codeph"> 0</span>이 사용됩니다. 장치가 가로 방향이면 무시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-10ee45d637134e0fbcd943c62578cb78}

선택 사항입니다.

## 기본값 {#section-d411e450028c460392cb8508f8ccc5d9}

기본값은 없습니다.

## 예 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
