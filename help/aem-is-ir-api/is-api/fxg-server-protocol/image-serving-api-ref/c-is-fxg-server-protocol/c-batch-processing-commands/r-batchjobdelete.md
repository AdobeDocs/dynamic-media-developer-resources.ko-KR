---
title: batchjobdelete
description: 작업 출력을 삭제합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
TQID: 'https://experienceleague.adobe.com/1UB1BxMzt2kGisK6gosRfoI1LEilkLyHJvfP1AJbwwI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

작업 출력을 삭제합니다.

작업이 현재 실행 중인 경우 즉시 중지되며 모든 처리 정보가 삭제됩니다. 작업이 성공적으로 완료되면 해당 출력 파일이 삭제됩니다.

이 매개 변수:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> job_id</span> </p> </td> 
  <td class="stentry"> <p>제출 시 획득한 작업 ID. </p></td> 
 </tr> 
</table>

반환:

`jobid`이(가) 잘못되었거나 작업이 이미 삭제된 경우 삭제 요청을 받은 시점의 작업 상태입니다.

## 예 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
