---
description: 새 배치 작업을 제출합니다.
solution: Experience Manager
title: batchjobsubmit
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 2%

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
