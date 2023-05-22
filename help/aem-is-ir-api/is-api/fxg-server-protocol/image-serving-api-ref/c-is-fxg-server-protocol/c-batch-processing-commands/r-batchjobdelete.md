---
description: 작업 출력을 삭제합니다.
solution: Experience Manager
title: batchjobdelete
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# batchjobdelete{#batchjobdelete}

작업 출력을 삭제합니다.

작업이 현재 실행 중인 경우 즉시 중지되며 모든 처리 정보가 삭제됩니다. 작업이 성공적으로 완료되면 해당 출력 파일이 삭제됩니다.

이 매개 변수:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 작업 ID</span> </p> </td> 
  <td class="stentry"> <p>제출 시 획득한 작업 ID. </p></td> 
 </tr> 
</table>

반환:

삭제 요청을 받은 시점의 작업 상태, 다음과 같은 경우 오류 발생 `jobid` 이(가) 잘못되었거나 작업이 이미 삭제되었습니다.

## 예 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
