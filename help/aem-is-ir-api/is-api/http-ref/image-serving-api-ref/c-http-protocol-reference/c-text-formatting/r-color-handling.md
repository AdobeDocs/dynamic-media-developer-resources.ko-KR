---
title: 색상 처리
description: RTF 사양은 &bsol;colortbl로 지정된 RGB 색상 값을 허용합니다. 각 구성 요소에는 &bsol;red, &bsol;green 및 &bsol;blue 명령이 별도로 제공됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# 색상 처리{#color-handling}

RTF 사양은 `\colortbl`(으)로 지정된 RGB 색상 값을 허용합니다. 각 구성 요소에는 `\red`, `\green` 및 `\blue` 명령이 별도로 제공됩니다.

전용 RTF 확장 명령 `\cmykcolortbl`을(를) 사용하면 각 색상 구성 요소에 `\cyan`, `\magenta`, `\yellow` 및 `\black` 명령을 제공하여 CMYK 색상을 지정할 수 있습니다.

`\colortbl`의 색상 구성 요소 값이 0-255 범위입니다. `\cmykcolortbl`의 구성 요소 값이 0-100 범위입니다.

`textPs=`이(가) 지원하는 RTF 확장 명령 `\*\iscolortbl`은(는) 전체 RGB, 회색, CMYK 및 알파 지원을 통해 표준 이미지 제공 색상 값으로 색상 테이블을 지정하는 방법을 제공합니다. 이 변수의 구문은 다음과 같습니다.

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* &#39;;&#39;로 구분된 하나 이상의 IS 색상 값

동일한 `text=` 또는 `textPs=` RTF 문자열에 두 개 이상의 유형의 색상표가 지정될 수 있습니다. 각 색상 테이블에는 다른 수의 항목이 있을 수 있습니다. 이미지 제공에서는 `\colortbl` 전에 `\cmykcolortbl` 이전 `\iscolortbl`(텍스트 레이어의 픽셀 유형이 CMYK인 경우에만) 순서로 색상을 찾으려고 합니다. `textPs=`의 경우에만 색상이 CMYK와 RGB 간에 정확하게 변환됩니다(필요한 경우)(예: RGB 색상이 지정되었지만 CMYK 출력이 필요한 경우). 특정 색인 값에 대한 색상이 없으면 기본 색상(검정)이 사용됩니다.

IS 색상 값 구문에 대한 설명은 [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)을(를) 참조하십시오.

## 제한 사항 {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 한정자는 `\*\iscolortbl`을(를) 지원하지 않습니다. `textPs=` 한정자는 `\cmykcolortbl`을(를) 지원하지 않습니다.

Photofonts를 렌더링할 때는 색상 선택이 무시됩니다.

## 예 {#section-0f166bb72bd44479be01131077851142}

표준 RTF 텍스트 편집기에서 RTF 문자열을 열 때 색상 기본값을 계속 표시하면서 변수로 세 텍스트 색상을 제어할 수 있습니다.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
