---
title: opac
description: 불투명도. 재료 불투명도를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# opac{#opac}

불투명도. 재료 불투명도를 지정합니다.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>재료 불투명도(퍼센트); 0...100 </p> </td> 
 </tr> 
</table>

다음 재료/개체 조합은 가변 불투명도를 지원합니다.

* 텍스처 겹치기 개체에 적용된 단색 및 반복 가능한 텍스쳐
* 윈도우 커버 프레임 객체에 적용되는 윈도우 커버 재료.
* 텍스쳐 객체 또는 벽 객체에 적용되는 디캘입니다.

자료에 알파 채널이 있는 이미지가 포함되어 있으면, `opac=` 이미지를 더 투명하게 만드는 데 사용할 수 있지만 더 불투명하지는 않습니다.

## 속성 {#section-352f7b82ede54159b6afb90ae4b559ec}

재료 속성입니다. 현재 개체 선택 또는 재료가 불투명도를 지원하지 않는 경우 무시됩니다.

## 기본값 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`- 완전히 불투명한 재질의 경우(이미지에 알파 채널이 포함되지 않은 경우)
