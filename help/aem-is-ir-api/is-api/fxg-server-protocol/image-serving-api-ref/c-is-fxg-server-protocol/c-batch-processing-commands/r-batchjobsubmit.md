---
description: 새 배치 작업을 제출합니다.
seo-description: 새 배치 작업을 제출합니다.
seo-title: batchjobsubmit
solution: Experience Manager
title: batchjobsubmit
topic: Scene7 Image Serving - Image Rendering API
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobsubmit{#batchjobsubmit}

새 배치 작업을 제출합니다.

이 매개 변수:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobdata </span> </p> </td> 
  <td class="stentry"> <p>전체 작업 데이터의 XML 조각. </p> </td> 
 </tr> 
</table>

반환:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>작업 상태 </p> </td> 
  <td class="stentry"> <p>제출 성공 또는 실패 여부성공한 경우 XML 형식의 작업 ID입니다. </p> </td> 
 </tr> 
</table>

## 예 {#section-3886e8352e26419c97b24df21ca7f6fd}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&amp;jobdata=<URLEncodedXMLFileContents>]
