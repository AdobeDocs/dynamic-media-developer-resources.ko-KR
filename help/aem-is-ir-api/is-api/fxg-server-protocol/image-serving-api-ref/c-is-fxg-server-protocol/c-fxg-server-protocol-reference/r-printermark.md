---
description: 프린터 표시를 표시합니다. 프린터 표시를 표시하는 방법을 지정합니다.
solution: Experience Manager
title: printerMark
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 31%

---

# printerMark{#printermark}

프린터 표시를 표시합니다. 프린터 표시를 표시하는 방법을 지정합니다.

` printerMark= *`trim `*, *`markdown `*, *`marketing`*, *`markdown`*, *`바코드 정보스타일`*, *``*, *`라인 `*, *`wearlayer 포함`*`

다른 표시는 꺼져 있거나 켜질 수 있습니다. 프린터 표시의 스타일을 제어할 수도 있습니다.

다음은 유효한 값입니다.

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>trim marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 0입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>bleed marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 0입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>registration marks= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 0입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>color bars= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 0입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>page information= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 0입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>기본값 </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>기본값은 기본값입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>line weight= </p></td> 
  <td class="stentry"> <p>0.125 - 2.0 범위의 값은 모두 포함되며, </p></td> 
  <td class="stentry"> <p>기본값은 0.25입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 1입니다. </p></td> 
 </tr> 
</table>

## 예 {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
