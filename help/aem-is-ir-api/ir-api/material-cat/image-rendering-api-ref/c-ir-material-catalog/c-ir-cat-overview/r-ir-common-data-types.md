---
description: 카탈로그 속성 및 필드에는 다음 유형 중 하나의 데이터가 포함될 수 있습니다.
solution: Experience Manager
title: 일반적인 데이터 유형
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# 일반적인 데이터 유형{#common-data-types}

카탈로그 속성 및 필드에는 다음 유형 중 하나의 데이터가 포함될 수 있습니다.

**색상**

색상 값. 16진수로 채워진 RGB 값(선택 사항: 0x) 앞에 와야 합니다. 예를 들어 RGB 값 `128,255,0`은 `0x80ff00` 또는 `80ff00`로 지정할 수 있습니다.

**플래그**

`0`= false,  `1`=true, 다른 값은 알 수 없거나 지정되지 않음을 의미합니다.

**열거형**

0은 빈 필드와 같은 알 수 없거나 지정되지 않은 값을 나타냅니다. 유효한 `enum` 값은 1부터 시작하여 연속되는 정수 숫자입니다.

**정수 숫자**

서명된 정수 값(예: 0, -12, 34). 0 또는 음수 값은 특별한 의미를 가질 수 있습니다.

**실수**

서명된 부동 소수점 값(예:`0, 12.5, 245 , -2.34e4`). 0 또는 음수 값은 특별한 의미를 가질 수 있습니다.

**텍스트 문자열**

문자열에 `<CR>`, `<LF>` 또는 `<TAB>` 문자가 포함되어 있지 않으면 문자열 구분 기호는 선택 사항입니다. 단일 및 큰따옴표는 구분 기호로 사용할 수 있습니다. 인용 부호를 사용하는 경우 문자열 내에 포함된 이러한 인용 부호는 연속적인 두 따옴표(예:&#39; `This month''s Special`&#39;).
