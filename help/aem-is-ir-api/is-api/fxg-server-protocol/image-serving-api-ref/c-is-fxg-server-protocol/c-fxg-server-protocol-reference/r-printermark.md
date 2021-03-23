---
description: 프린터 표시를 표시합니다. 프린터 표시를 표시하는 방법을 지정합니다.
seo-description: 프린터 표시를 표시합니다. 프린터 표시를 표시하는 방법을 지정합니다.
seo-title: printerMark
solution: Experience Manager
title: printerMark
uuid: 3e5699ce-3ccd-4f85-91dd-c40c252a758d
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 28%

---


# printerMark{#printermark}

프린터 표시를 표시합니다. 프린터 표시를 표시하는 방법을 지정합니다.

` printerMark= *`트리밍 `*, *`마크도련 `*, *`마크등록 `*, *`마커 `*, *`바스페이지 `*, *``*, *`정보 스타일라인 `*, *`웨이레이어 임베드`*`

다른 표시는 꺼지거나 켜질 수 있습니다. 프린터 표시 스타일도 제어할 수 있습니다.

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
