---
description: 포커스가 있는 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 초점 강조 표시는 CSS 클래스 선택기로 제어됩니다.
seo-description: 포커스가 있는 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 초점 강조 표시는 CSS 클래스 선택기로 제어됩니다.
seo-title: 초점 강조 표시
solution: Experience Manager
title: 초점 강조 표시
uuid: 99d822b5-29ea-4229-8eb8-e3903322b7fa
feature: Dynamic Media Classic,뷰어,SDK/API,360 VR 비디오
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# 초점 강조 표시{#focus-highlight}

포커스가 있는 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 초점 강조 표시는 CSS 클래스 선택기로 제어됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS 속성**

모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7video360viewer *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS 속성 </p> </th> 
   <th colname="col2" class="entry"> <p>설명 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 윤곽선  </span> </p> </td> 
   <td colname="col2"> <p>초점 밝은 영역 스타일입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 모든 뷰어 사용자 인터페이스 요소에 대한 기본 브라우저 초점 하이라이트를 비활성화하려면 뷰어의 스타일 시트에 다음 CSS 선택기를 추가하십시오.

```
.s7video360viewer *:focus { 
 outline: none; 
}
```

