---
description: 프린터 표시를 표시합니다. 프린터 표시를 표시하는 방법을 지정합니다.
solution: Experience Manager
title: 프린터 표시
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f61c7311-a2e9-4eb7-ae05-276a4eec980b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# 프린터 표시{#printermark}

프린터 표시를 표시합니다. 프린터 표시를 표시하는 방법을 지정합니다.

` printerMark= *`재단 표시`*, *`재단 표시`*, *`등록 표시`*, *`색상 막대`*, *`페이지 정보`*, *`스타일`*, *`선 두께`*, *`레이어 포함`*`

다른 표시를 끄거나 켤 수 있습니다. 프린터 표시의 스타일도 제어할 수 있습니다.

다음은 유효한 값입니다.

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>트리밍 표시= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 0입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>재단 물림 기호= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 0입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>등록 표시= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 0입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>색상 막대= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 0입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>페이지 정보= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>기본값은 0입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>기본값 </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>기본값은 기본입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>선 두께= </p></td> 
  <td class="stentry"> <p>0.125 - 2.0 범위의 모든 값(두 값 모두 포함). </p></td> 
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
