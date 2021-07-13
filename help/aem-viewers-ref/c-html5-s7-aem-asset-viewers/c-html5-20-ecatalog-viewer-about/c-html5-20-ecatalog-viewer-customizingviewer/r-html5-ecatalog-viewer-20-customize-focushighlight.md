---
description: 포커스가 있는 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 포커스 강조 표시입니다.
solution: Experience Manager
title: 포커스 강조 표시
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# 포커스 강조 표시{#focus-highlight}

포커스가 있는 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 포커스 강조 표시입니다.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

포커스 강조 표시의 모양은 다음 CSS 클래스 선택기로 제어됩니다.

```
.s7ecatalogviewer *:focus
```

**초점 강조 표시의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 개요  </span> </p> </td> 
   <td colname="col2"> <p> 초점 강조 스타일. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 모든 뷰어 사용자 인터페이스 요소에 대해 기본 브라우저 포커스 강조 표시를 비활성화하려면 다음 CSS 선택기를 뷰어의 스타일 시트에 추가합니다.

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
