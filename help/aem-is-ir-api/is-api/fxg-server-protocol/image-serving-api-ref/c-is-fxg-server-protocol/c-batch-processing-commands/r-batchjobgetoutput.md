---
description: 제출된 작업의 출력을 검색합니다.
solution: Experience Manager
title: batchjobgetoutput
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fb48c39-b15a-45b7-9aca-ed33f9c46c93
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---

# batchjobgetoutput{#batchjobgetoutput}

제출된 작업의 출력을 검색합니다.

이 매개 변수:

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>제출 시 얻은 작업 ID. </p> </td> 
 </tr> 
</table>

반환:

작업의 PDF 출력이 응답으로 스트리밍됩니다. 오류: `jobid` 이 잘못되었거나 작업이 삭제되었습니다.

## 예 {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
