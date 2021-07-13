---
description: 대체 문자열 요소입니다. <규칙> 요소에서 선택 사항입니다.
solution: Experience Manager
title: 대체
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 3%

---

# 대체{#substitution}

대체 문자열 요소입니다. `<rule>` 요소에서 선택 사항입니다.

## 속성 {#section-d955eefc53eb4274861270669c01f9ca}

없음.

## 데이터 {#section-a2688866ed6d41279a8478886e511ae3}

대체 문자열입니다.

## 설명 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

경로 또는 쿼리에서 일치하는 문자열 또는 하위 문자열에 대한 대체 문자열을 정의합니다.

패턴 표현식에 하위 표현식(괄호로 구분됨)이 포함되어 있으면 첫 번째 일치하는 하위 문자열이 대체 문자열로 대체됩니다. 패턴 표현식에 하위 표현식이 포함되지 않으면 일치하는 전체 문자열이 대체됩니다.

`<expression>` 이 비어 있거나 없는 경우 대체 문자열이 경로 또는 쿼리에 추가됩니다.

`<substitution>`이 비어 있으면 일치하는 문자열 또는 하위 문자열이 제거됩니다. `<substitution>`을 지정하지 않으면 경로나 쿼리 문자열이 수정되지 않습니다.

## 참고 {#section-90fe89bb17a04804b7ff3c93df082892}

대체 문자열은 리터럴 &lt; 및 문자를 포함하지 않아야 합니다. 이러한 예약된 문자는 각각 `&` 및 `<` 로 인코딩하거나 전체 문자열을 XML `CDATA` 섹션에 묶을 수 있습니다.

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
