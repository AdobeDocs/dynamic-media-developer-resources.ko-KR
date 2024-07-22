---
title: opac
description: 불투명도. 재질 불투명도를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# opac{#opac}

불투명도. 재질 불투명도를 지정합니다.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 값 </span> </p> </td> 
  <td class="stentry"> <p>재질 불투명도(백분율); 0...100 </p> </td> 
 </tr> 
</table>

다음 재료/개체 조합은 가변 불투명도를 지원합니다.

* 텍스처 중첩 개체에 적용된 단색 및 반복 가능한 텍스처.
* 창 커버링 프레임 객체에 적용된 창 커버링 재료입니다.
* 텍스처 개체 또는 벽 개체에 적용된 데칼.

물체에 알파 채널이 있는 이미지가 포함된 경우 `opac=`을(를) 사용하여 이미지를 더 투명하게 만들 수 있지만 더 불투명하게 만들 수는 없습니다.

## 속성 {#section-352f7b82ede54159b6afb90ae4b559ec}

재질 속성입니다. 현재 오브젝트 선택 영역이나 재료가 불투명도를 지원하지 않는 경우에는 무시됩니다.

## 기본값 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`(이미지에 알파 채널이 없는 경우).
