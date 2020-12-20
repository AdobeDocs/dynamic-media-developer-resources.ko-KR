---
description: 제출한 작업의 세부 상태를 검색합니다.
seo-description: 제출한 작업의 세부 상태를 검색합니다.
seo-title: batchjobdetailedstatus
solution: Experience Manager
title: batchjobdetailedstatus
topic: Scene7 Image Serving - Image Rendering API
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 1%

---


# batchjobdetailestatus{#batchjobdetailedstatus}

제출한 작업의 세부 상태를 검색합니다.

이 매개 변수:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 조비드  </span> </p> </td> 
  <td class="stentry"> <p>제출 시 획득한 작업 ID. </p> </td> 
 </tr> 
</table>

반환:

XML 형식의 작업 세부 상태;오류: `jobid`이(가) 잘못되었거나 작업이 삭제된 경우

## 예 {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
