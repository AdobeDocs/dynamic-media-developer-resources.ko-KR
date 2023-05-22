---
description: Jpeg 품질입니다. 압축 수준을 제어할 JPEG 인코딩 특성을 지정합니다. 이렇게 하면 파일 크기(응답 데이터의 양)와 결과 이미지의 시각적 품질이 간접적으로 달라집니다.
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 15%

---

# qlt{#qlt}

Jpeg 품질입니다. 압축 수준을 제어할 JPEG 인코딩 특성을 지정합니다. 이렇게 하면 파일 크기(응답 데이터의 양)와 결과 이미지의 시각적 품질이 간접적으로 달라집니다.

` qlt= *`품질`*[, *`색도`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 품질 </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG 인코딩 품질(1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 색도 </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG 색도 다운샘플링(0=보통, 1=비활성화), 선택 사항, 기본값은 0입니다. </p> </td> 
 </tr> 
</table>

다음과 같은 경우에만 사용됨 `fmt=jpg`. 그렇지 않으면 무시됨

품질 값이 크면 파일 크기가 증가하고 품질이 향상되며, 값이 작으면 파일 크기가 감소하고 인식되는 이미지 품질이 저하됩니다. 값이 90보다 큰 경우 압축되지 않은 이미지와 구분할 수 없는 이미지가 생성되는 경우가 많습니다.

설정 `chroma` 일반적인 JPEG 인코더에서 사용하는 RGB 색도 다운샘플링을 비활성화하는 플래그입니다. 이는 에지가 밝기보다 색조의 변화에 의해 정의될 때 이미지 내의 에지의 지각된 선명도를 증가시킬 수 있다. 이 플래그를 설정하면 파일 크기가 약간 증가할 수 있습니다. 텍스트가 약간 흐리게 보이는 경우 이 설정을 실험해 보십시오.

`chroma` 출력 픽셀 유형이 CMYK 또는 회색인 경우 이 무시됩니다.

## 예 {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
