---
description: 불투명도. 질감 불투명도를 지정합니다.
seo-description: 불투명도. 질감 불투명도를 지정합니다.
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f5b11f0-af65-4abd-947e-7a28cb8de263
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# opac{#opac}

불투명도. 질감 불투명도를 지정합니다.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>질감 불투명도(퍼센트);0...100 </p> </td> 
 </tr> 
</table>

다음 재료/개체 조합은 가변 불투명도를 지원합니다.

* 텍스처 가능한 오버랩 개체에 적용된 단색 및 반복 가능한 텍스처
* 창 커버링 프레임 오브젝트에 적용된 윈도우 적용 재료.
* 텍스처 가능한 개체 또는 벽 개체에 적용된 디캘입니다.

자료에 알파 채널이 있는 이미지가 포함된 경우 이미지를 보다 투명하게 만드는 데 사용할 `opac=` 수 있지만 더 이상 불투명하지 않습니다.

## 속성 {#section-352f7b82ede54159b6afb90ae4b559ec}

재료 속성. 현재 개체 선택 사항이나 재질이 불투명도를 지원하지 않는 경우 무시됩니다.

## 기본값 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`에 대해 를 지정합니다.
