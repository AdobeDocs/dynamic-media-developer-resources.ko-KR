---
description: 초점이 맞춰진 뷰어 UI 요소 주위에 표시되는 입력 초점 강조 표시는 CSS 클래스 선택기로 제어됩니다.
seo-description: 초점이 맞춰진 뷰어 UI 요소 주위에 표시되는 입력 초점 강조 표시는 CSS 클래스 선택기로 제어됩니다.
seo-title: 초점 강조 표시
solution: Experience Manager
title: 초점 강조 표시
topic: Dynamic media
uuid: 04358471-537d-4904-9775-db6a6ada2204
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 초점 강조 표시{#focus-highlight}

초점이 맞춰진 뷰어 UI 요소 주위에 표시되는 입력 초점 강조 표시는 CSS 클래스 선택기로 제어됩니다.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS 속성**

모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7flyoutviewer *:focus
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
   <td colname="col1"> <p> <span class="codeph"> 윤곽선 </span> </p> </td> 
   <td colname="col2"> <p>초점 강조 스타일. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 모든 뷰어 사용자 인터페이스 요소에 대한 기본 브라우저 초점 강조 표시를 비활성화하려면 다음 CSS 선택기를 뷰어의 스타일 시트에 추가합니다.

```
.s7flyoutviewer *:focus { 
 outline: none; 
}
```

