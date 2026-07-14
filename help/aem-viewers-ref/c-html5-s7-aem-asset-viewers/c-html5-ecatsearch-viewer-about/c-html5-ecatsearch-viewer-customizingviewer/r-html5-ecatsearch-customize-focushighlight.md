---
title: 포커스 강조 표시
description: 포커싱된 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 포커스 강조 표시입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
TQID: 'https://experienceleague.adobe.com/E7n09sJ0qY9Aivp5OUFr5Jc6bwS5Ah3N-HdS9-H2Pgw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 74
ht-degree: 0%

---

# 포커스 강조 표시{#focus-highlight}

포커싱된 뷰어 사용자 인터페이스 요소 주위에 표시되는 입력 포커스 강조 표시입니다.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

다음 CSS 클래스 선택기를 사용하여 포커스 강조 표시의 모양이 제어됩니다.

```
.s7ecatalogviewer *:focus
```

**포커스 강조 표시의 CSS 속성**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 개요 </span> </p> </td> 
   <td colname="col2"> <p> 포커스 강조 표시 스타일입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

예 - 모든 뷰어 사용자 인터페이스 요소에 대한 기본 브라우저 포커스 강조 표시를 비활성화하려면 다음 CSS 선택기를 뷰어의 스타일 시트에 추가합니다.

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
