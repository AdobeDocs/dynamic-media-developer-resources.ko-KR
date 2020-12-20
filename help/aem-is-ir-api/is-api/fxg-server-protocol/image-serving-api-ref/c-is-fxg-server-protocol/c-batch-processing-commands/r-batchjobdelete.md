---
description: 작업 출력을 삭제합니다.
seo-description: 작업 출력을 삭제합니다.
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
topic: Scene7 Image Serving - Image Rendering API
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 1%

---


# batchjobdelete{#batchjobdelete}

작업 출력을 삭제합니다.

현재 작업이 실행 중인 경우 즉시 중지되고 모든 처리 정보가 삭제됩니다. 작업이 성공적으로 완료되면 출력 파일이 삭제됩니다.

이 매개 변수:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 조비드</span> </p> </td> 
  <td class="stentry"> <p>제출 시 획득한 작업 ID. </p></td> 
 </tr> 
</table>

반환:

삭제 요청을 받은 때의 작업 상태, `jobid`이(가) 잘못되었거나 작업이 이미 삭제되었을 때 오류가 발생했습니다.

## 예 {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
