---
description: 제출된 작업의 세부 상태를 검색합니다.
solution: Experience Manager
title: batchjobdetailedstatus
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: fd385327-29af-448c-9a25-75098b578272
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 1%

---

# batchjobdetailedstatus{#batchjobdetailedstatus}

제출된 작업의 세부 상태를 검색합니다.

이 매개 변수:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>제출 시 얻은 작업 ID. </p> </td> 
 </tr> 
</table>

반환:

XML 형식으로 작업의 세부 상태오류: `jobid` 이 잘못되었거나 작업이 삭제되었습니다.

## 예 {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
