---
description: 모든 뷰어에 공통되는 매개 변수입니다.
seo-description: 모든 뷰어에 공통되는 매개 변수입니다.
seo-title: initialFrame
solution: Experience Manager
title: initialFrame
topic: Dynamic media
uuid: 5d1c3a8a-8598-47c9-a106-36e8c6fcafb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# initialFrame{#initialframe}

모든 뷰어에 공통되는 매개 변수입니다.

>[!NOTE]
>
>이 명령은 비디오 이미지 뷰어에 적용되지 않습니다.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> 뷰어가 로드 시 표시하는 0부터 시작하는 프레임 인덱스를 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>장치가 세로 방향일 때 스프레드 내 페이지의 인덱스(0부터 시작). "왼쪽에서 오른쪽" 환경에서 <span class="codeph"> 0</span>은 "왼쪽 페이지"를 의미하고 <span class="codeph"> 1</span>은 "오른쪽 페이지"를 의미합니다. "오른쪽에서 왼쪽으로"는 반대입니다.<span class="codeph"> 0</span>은 "오른쪽 페이지"를 의미하고 <span class="codeph"> 1</span>은 "왼쪽 페이지"를 의미합니다. </p> <p>지정하지 않으면 기본적으로 <span class="codeph"> 0</span>이(가) 사용됩니다. 장치가 가로 방향일 때 무시됩니다. </p> </td> 
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

