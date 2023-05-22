---
description: RTF 사양은 &bsol;colortbl로 지정된 RGB 색상 값을 허용합니다. 각 구성 요소에는 &bsol;red, &bsol;green 및 &bsol;blue 명령이 별도로 제공됩니다.
solution: Experience Manager
title: 색상 처리
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# 색상 처리{#color-handling}

RTF 사양은 RGB 색상 값을 `\colortbl`. 각 구성 요소에는 `\red`, `\green`, 및 `\blue` 명령입니다.

전용 RTF 확장 명령 `\cmykcolortbl` 각 색상 구성 요소에 CMYK 색상을 지정할 수 있습니다. `\cyan`, `\magenta`, `\yellow`, 및 `\black` 명령입니다.

색상 구성 요소 값 `\colortbl` 은(는) 0에서 255 사이의 범위에 있습니다. 구성 요소 값 `\cmykcolortbl` 은(는) 0에서 100 사이의 범위에 있습니다.

RTF 확장 명령 `\*\iscolortbl`, 지원자 `textPs=`는 전체 RGB, 회색, CMYK 및 알파 지원을 통해 표준 이미지 제공 색상 값으로 색상 테이블을 지정하는 방법을 제공합니다. 이 변수의 구문은 다음과 같습니다.

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* &#39;;&#39;로 구분된 하나 이상의 IS 색상 값

두 개 이상의 색상 테이블 유형을 동일한 위치에 지정할 수 있습니다 `text=` 또는 `textPs=` RTF 문자열. 각 색상 테이블에는 다른 수의 항목이 있을 수 있습니다. 이미지 제공에서는 다음 순서로 색상 검색을 시도합니다. `\iscolortbl` 다음 이전 `\cmykcolortbl` (텍스트 레이어의 픽셀 유형이 CMYK인 경우에만) `\colortbl`. 대상 `textPs=` 필요한 경우(예: RGB 색상이 지정되었지만 CMYK 출력이 필요한 경우) 색상은 CMYK와 RGB 간에 정확하게 변환됩니다. 특정 색인 값에 대한 색상이 없으면 기본 색상(검정)이 사용됩니다.

을(를) 참조하십시오 [색상](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) IS 색상 값 구문에 대한 설명입니다.

## 제한 사항 {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 은(는) 을 지원하지 않습니다. `\*\iscolortbl`. `textPs=` 은(는) 을 지원하지 않습니다. `\cmykcolortbl`.

Photofonts를 렌더링할 때는 색상 선택이 무시됩니다.

## 예 {#section-0f166bb72bd44479be01131077851142}

표준 RTF 텍스트 편집기에서 RTF 문자열을 열 때 색상 기본값을 계속 표시하면서 변수로 세 텍스트 색상을 제어할 수 있습니다.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
