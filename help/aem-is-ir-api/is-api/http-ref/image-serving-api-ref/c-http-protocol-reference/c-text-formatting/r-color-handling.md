---
description: RTF 사양은 &bsol;colortbl에 지정된 RGB 색상 값을 허용합니다. 각 구성 요소는 &bsol;red, &bsol;green 및 &bsol;blue 명령과 별도로 제공됩니다.
solution: Experience Manager
title: 색상 처리
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# 색상 처리{#color-handling}

RTF 사양은 `\colortbl`에 지정된 RGB 색상 값을 허용합니다. 각 구성 요소는 `\red`, `\green` 및 `\blue` 명령과 별도로 제공됩니다.

자체 RTF 확장 명령 `\cmykcolortbl`을 사용하면 `\cyan`, `\magenta`, `\yellow` 및 `\black` 명령과 함께 각 색상 구성 요소를 사용하여 CMYK 색상을 지정할 수 있습니다.

`\colortbl`의 색상 구성 요소 값은 0에서 255 범위에 있습니다. `\cmykcolortbl`의 구성 요소 값은 0에서 100 사이여야 합니다.

`textPs=`에서 지원하는 RTF 확장 명령 `\*\iscolortbl`을 사용하면 전체 RGB, 회색, CMYK 및 알파 지원을 제공하는 표준 이미지 제공 색상 값이 있는 색상 테이블을 지정할 수 있습니다. 여기에는 다음 구문이 있습니다.

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 하나 이상의 IS 색상 값이 &#39;;&#39;로 구분되어 있습니다.

동일한 `text=` 또는 `textPs=` RTF 문자열에 둘 이상의 색상 테이블을 지정할 수 있습니다. 각 색상 테이블에는 서로 다른 수의 항목이 있을 수 있습니다. 이미지 제공에서 다음 순서로 색상을 찾습니다. `\iscolortbl` 앞에 `\cmykcolortbl` (텍스트 레이어의 픽셀 유형이 CMYK인 경우에만) `\colortbl` 앞에 있습니다. `textPs=`의 경우에만 필요한 경우 CMYK와 RGB 간에 색상이 정확하게 변환됩니다(예: RGB 색상을 지정하지만 CMYK 출력이 필요한 경우). 특정 인덱스 값에 대한 색상이 없으면 기본 색상(검정)이 사용됩니다.

IS 색상 값의 구문에 대한 설명은 [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 를 참조하십시오.

## 제한 사항 {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 은 를 지원하지 않습니다  `\*\iscolortbl`. `textPs=` 은 를 지원하지 않습니다  `\cmykcolortbl`.

Photoshop 글꼴을 렌더링할 때는 색상 선택이 무시됩니다.

## 예 {#section-0f166bb72bd44479be01131077851142}

표준 RTF 텍스트 편집기에서 RTF 문자열을 열 때 색상 기본값을 표시하는 동안 세 가지 텍스트 색상을 변수로 제어할 수 있습니다.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
