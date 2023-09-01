---
title: 대체
description: 대체 문자열 요소입니다. 에서 선택 사항 <rule> 요소.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# 대체{#substitution}

대체 문자열 요소입니다. 에서 선택 사항 `<rule>` 요소.

## 속성 {#section-d955eefc53eb4274861270669c01f9ca}

없음.

## 데이터 {#section-a2688866ed6d41279a8478886e511ae3}

대체 문자열.

## 설명 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

경로 또는 쿼리에서 일치하는 문자열 또는 하위 문자열에 대한 대체 문자열을 정의합니다.

패턴 표현식에 하위 표현식(괄호로 구분)이 포함된 경우 첫 번째 일치하는 하위 문자열은 대체 문자열로 대체됩니다. 패턴 표현식에 하위 표현식이 포함되지 않으면 일치하는 전체 문자열이 대체됩니다.

If `<expression>` 가 비어 있거나 없으면 대체 문자열이 경로 또는 쿼리에 추가됩니다.

If `<substitution>` 이(가) 비어 있으면 일치하는 문자열 또는 하위 문자열이 제거됩니다. If `<substitution>` 이 지정되지 않았거나 경로 또는 쿼리 문자열이 수정되지 않았습니다.

## 참고 {#section-90fe89bb17a04804b7ff3c93df082892}

대체 문자열은 리터럴 &lt; 및 &amp; 문자를 포함하지 않아야 합니다. 예약된 이러한 문자는 `&` 및 `<`, 각각 또는 전체 문자열을 XML로 묶을 수 있습니다 `CDATA` 섹션:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
