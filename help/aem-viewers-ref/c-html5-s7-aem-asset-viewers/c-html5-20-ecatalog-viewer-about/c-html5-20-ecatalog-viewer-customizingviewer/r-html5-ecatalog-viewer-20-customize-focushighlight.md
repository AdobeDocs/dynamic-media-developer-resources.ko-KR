---
description: 초점을 맞춘 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 초점 강조 표시
seo-description: 초점을 맞춘 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 초점 강조 표시
seo-title: 초점 강조 표시
solution: Experience Manager
title: 초점 강조 표시
topic: Dynamic media
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 초점 강조 표시{#focus-highlight}

초점을 맞춘 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 초점 강조 표시

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

초점 강조 표시의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer *:focus
```

**초점 강조 표시의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 윤곽선 </span> </p> </td> 
   <td colname="col2"> <p> 초점 강조 스타일. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 모든 뷰어 사용자 인터페이스 요소에 대한 기본 브라우저 초점 강조 표시를 비활성화하려면 뷰어의 스타일 시트에 다음 CSS 선택기를 추가합니다.

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

