---
description: 새 배치 작업을 제출합니다.
seo-description: 새 배치 작업을 제출합니다.
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 1%

---


# batchjobsubmit{#batchjobsubmit}

새 배치 작업을 제출합니다.

이 매개 변수:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata  </span> </p> </td> 
  <td class="stentry"> <p>전체 작업 데이터의 XML 조각. </p> </td> 
 </tr> 
</table>

반환:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>작업 상태 </p> </td> 
  <td class="stentry"> <p>제출이 성공했는지 실패했는지 여부;성공한 경우 작업 ID를 XML 형식으로 표시합니다. </p> </td> 
 </tr> 
</table>

## 예 {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
