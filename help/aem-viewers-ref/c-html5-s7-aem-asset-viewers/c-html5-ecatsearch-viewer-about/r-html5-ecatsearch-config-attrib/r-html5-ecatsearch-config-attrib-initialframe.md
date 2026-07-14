---
description: 초기 프레임
solution: Experience Manager
title: 초기 프레임
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 15241738-a1b6-4723-b6fc-ebc8f7dedb03
TQID: 'https://experienceleague.adobe.com/mOv0xdpEX6HFHvTkn09jtFwxAYwKJcFPv0O5iVu-PP8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 59
ht-degree: 5%

---

# 초기 프레임{#initialframe}

[!DNL ` initialFrame= *`프레임`*`]

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 프레임</span></span> </p> </td> 
   <td colname="col2"> <p> 뷰어 로드 시 표시할 0부터 시작하는 확산 인덱스를 지정합니다. 이 지수는 가로 모드에서의 스프레드 지수와 일치합니다. 뷰어를 세로로 회전하면 뷰어는 <span class="codeph"> frameIdx</span>이 가리키는 스프레드의 가장 왼쪽 페이지를 표시합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-fc7c012c91d1419b8a5bb60d28e17327}

선택적.

## 기본값 {#section-bbc6ebad3af54fd79837515c270e6ddf}

[!DNL `0`]

## 예 {#section-cbc6684eb22e4d0883edc4b3d5742336}

뷰어 URL에 지정되는 경우.

```
[!DNL initialFrame=2
```

