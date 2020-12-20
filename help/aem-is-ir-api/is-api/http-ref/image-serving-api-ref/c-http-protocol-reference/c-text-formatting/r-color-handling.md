---
description: RTF 사양은 &bsol;colortbl과 함께 지정된 RGB 색상 값을 허용합니다. 각 구성 요소는 &bsol;red, &bsol;green, &bsol;blue 명령을 사용하여 별도로 제공됩니다.
solution: Experience Manager
title: 색상 처리
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 925fb4b0a9018d711ea9a1db248dc2ddc803c9fb
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# 색상 처리{#color-handling}

RTF 사양에서는 `\colortbl`으로 지정된 RGB 색상 값을 허용합니다. 각 구성 요소는 `\red`, `\green` 및 `\blue` 명령과 별도로 제공됩니다.

전용 RTF 확장 명령 `\cmykcolortbl`을 사용하면 `\cyan`, `\magenta`, `\yellow` 및 `\black` 명령과 함께 제공되는 각 색상 구성 요소를 사용하여 CMYK 색상을 지정할 수 있습니다.

`\colortbl`의 색상 구성 요소 값은 0에서 255 범위의 값입니다. `\cmykcolortbl`의 구성 요소 값은 0에서 100 사이여야 합니다.

`textPs=`에서 지원하는 RTF 확장 명령 `\*\iscolortbl`은 전체 RGB, 회색, CMYK 및 알파 지원을 통해 표준 이미지 제공 색상 값을 포함하는 색상 표를 지정하는 방법을 제공합니다. 여기에는 다음 구문이 있습니다.

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 하나 이상의 IS 색상 값이 &#39;;&#39;으로 구분되어 있습니다.

동일한 `text=` 또는 `textPs=` RTF 문자열에 둘 이상의 색상 표 유형을 지정할 수 있습니다. 각 색상표에는 항목 수가 다를 수 있습니다. 이미지 제공에서 다음 순서로 색상을 찾습니다.`\cmykcolortbl` 이전 `\iscolortbl`(텍스트 레이어의 픽셀 유형이 CMYK인 경우에만 해당) `\colortbl` 앞에 있습니다. `textPs=`의 경우에만 필요한 경우 CMYK와 RGB 간에 색상이 정확하게 변환됩니다(예: RGB 색상이 지정되었지만 CMYK 출력이 필요한 경우). 특정 인덱스 값에 대한 색상이 없으면 기본 색상(검정)이 사용됩니다.

IS 색상 값의 구문에 대한 설명은 [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)을 참조하십시오.

## 제한 사항 {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 을 지원하지 않습니다 `\*\iscolortbl`. `textPs=` 을 지원하지 않습니다 `\cmykcolortbl`.

Photoshop 글꼴을 렌더링할 때는 색상 선택이 무시됩니다.

## 예 {#section-0f166bb72bd44479be01131077851142}

표준 RTF 텍스트 편집기에서 RTF 문자열을 열 때 색상 기본값을 표시하는 반면, 3개의 텍스트 색상을 변수로 제어할 수 있습니다.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
