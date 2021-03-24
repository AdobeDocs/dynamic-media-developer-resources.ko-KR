---
description: 포커스가 있는 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 초점 하이라이트입니다.
solution: Experience Manager
title: 초점 강조 표시
feature: Dynamic Media Classic,뷰어,SDK/API,eCatalog 검색
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# 초점 강조 표시{#focus-highlight}

포커스가 있는 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 초점 하이라이트입니다.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

초점 강조 표시의 모양은 다음과 같은 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer *:focus
```

**초점 강조 표시의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 윤곽선  </span> </p> </td> 
   <td colname="col2"> <p> 초점 밝은 영역 스타일입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 모든 뷰어 사용자 인터페이스 요소에 대한 기본 브라우저 초점 하이라이트를 비활성화하려면 뷰어의 스타일 시트에 다음 CSS 선택기를 추가합니다.

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

