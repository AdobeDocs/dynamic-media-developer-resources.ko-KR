---
title: batchjobbriefstatus
description: 제출된 작업의 요약된 상태를 검색합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
source-git-commit: 13991f71ab54d1003a79a496b861d53a61899bdc
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 2%

---

# batchjobbriefstatus{#batchjobbriefstatus}

제출된 작업의 요약된 상태를 검색합니다.

이 매개 변수:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 작업 ID </span> </p> </td> 
  <td class="stentry"> <p>제출 시 획득한 작업 ID. </p> </td> 
 </tr> 
</table>

반환:

작업 XML 형식의 간략한 상태. 작업 ID가 잘못되었거나 작업이 삭제된 경우 오류가 발생합니다.

## 예 {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
