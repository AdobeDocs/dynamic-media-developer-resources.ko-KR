---
description: 제출된 작업의 요약된 상태를 검색합니다.
solution: Experience Manager
title: batchjobapstatus
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---


# batchjobformstatus{#batchjobbriefstatus}

제출된 작업의 요약된 상태를 검색합니다.

이 매개 변수:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 조비드  </span> </p> </td> 
  <td class="stentry"> <p>제출 시 획득한 작업 ID. </p> </td> 
 </tr> 
</table>

반환:

XML 형식의 간략한 작업 상태;jobid가 잘못되었거나 작업이 삭제된 경우 오류가 발생했습니다.

## 예 {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
