---
description: 대체 문자열 요소입니다. <규칙> 요소에서 선택 사항입니다.
solution: Experience Manager
title: 대체
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# 대체{#substitution}

대체 문자열 요소입니다. `<rule>` 요소에서 선택 사항입니다.

## 속성 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

없음.

## 데이터 {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

대체 문자열입니다.

## 설명 {#section-4a64a93f5e1a4d04a2db19166578bf76}

경로 또는 쿼리에서 일치하는 문자열 또는 하위 문자열에 대한 대체 문자열을 정의합니다.

패턴 표현식에 하위 표현식(괄호로 구분됨)이 포함되어 있으면 첫 번째 일치하는 하위 문자열이 대체 문자열로 대체됩니다. 패턴 표현식에 하위 표현식이 포함되지 않으면 일치하는 전체 문자열이 대체됩니다.

`<expression>` 이 비어 있거나 없는 경우 대체 문자열이 경로 또는 쿼리에 추가됩니다.

`<substitution>`이 비어 있으면 일치하는 문자열 또는 하위 문자열이 제거됩니다. `<substitution>`을 지정하지 않으면 경로나 쿼리 문자열이 수정되지 않습니다.

>[!NOTE]
>
>`<rule>` 이 `<substitution>` 요소가 속한 요소에 `replace="all"`이 지정되면 입력 문자열의 모든 일치가 대체됩니다. 기본적으로 첫 번째 일치만 대체 문자열로 대체됩니다.

## 참고 {#section-cedf2adabaaf441c9f598fb0ea180246}

대체 문자열은 리터럴 &lt; 및 문자를 포함하지 않아야 합니다. 이러한 예약된 문자는 각각 `&` 및 `<` 로 인코딩하거나 전체 문자열을 XML CDATA 섹션에 묶을 수 있습니다.

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
