---
description: 새 일괄 처리 작업을 제출합니다.
solution: Experience Manager
title: 일괄 작업 제출
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ab2f6e4-cd68-4f1e-ab54-6f5e9bfc87cb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '38'
ht-degree: 2%

---

# 일괄 작업 제출{#batchjobsubmit}

새 일괄 처리 작업을 제출합니다.

이 매개 변수:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 작업 데이터 </span> </p> </td> 
  <td class="stentry"> <p>전체 작업 데이터의 XML 조각입니다. </p> </td> 
 </tr> 
</table>

반환:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>작업 상태 </p> </td> 
  <td class="stentry"> <p>제출 성공 또는 실패 여부, 성공하면 XML 형식의 작업 ID입니다. </p> </td> 
 </tr> 
</table>

## 예 {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
