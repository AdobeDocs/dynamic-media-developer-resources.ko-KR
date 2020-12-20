---
description: 제출된 작업의 출력을 검색합니다.
seo-description: 제출된 작업의 출력을 검색합니다.
seo-title: batchjobogetoutput
solution: Experience Manager
title: batchjobogetoutput
topic: Scene7 Image Serving - Image Rendering API
uuid: c2d49cc2-3223-4f0f-8ba7-4f74a5f76789
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---


# batchjobogetoutput{#batchjobgetoutput}

제출된 작업의 출력을 검색합니다.

이 매개 변수:

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 조비드  </span> </p> </td> 
  <td class="stentry"> <p>제출 시 획득한 작업 ID. </p> </td> 
 </tr> 
</table>

반환:

작업의 PDF 출력은 응답으로 스트리밍됩니다.오류: `jobid`이(가) 잘못되었거나 작업이 삭제된 경우

## 예 {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
