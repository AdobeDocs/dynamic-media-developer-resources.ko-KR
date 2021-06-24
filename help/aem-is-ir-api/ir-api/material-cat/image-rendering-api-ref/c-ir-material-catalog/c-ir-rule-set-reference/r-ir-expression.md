---
description: 정규 표현식 패턴 요소. <규칙> 요소에서 선택 사항입니다.
solution: Experience Manager
title: 식
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 4%

---

# 식{#expression}

정규 표현식 패턴 요소. `<rule>` 요소에서 선택 사항입니다.

## 속성 {#section-fd0574eee1f9423cbb2ed709c0906800}

없음.

## 데이터 {#section-4cd740c511a1432da0955e9acfbcf96f}

정규 표현식 패턴 문자열입니다.

## 설명 {#section-3245c8a531bb455d8398449f6ea63b37}

`<expression>` 요소는 비어 있거나 단순 검색 문자열 또는 정규 표현식 패턴을 포함할 수 있습니다. 패턴은 전체 요청 문자열에 적용됩니다.

`<expression>`이 비어 있거나 지정되지 않은 경우 항상 일치 항목이 발생합니다.이는 `<expression>.*</expression>` 을 지정하는 것과 같습니다.

이 구현은 Perl과 유사한 정규 표현식 구문을 제공하는 Java 패키지 [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)을 기반으로 합니다.

## 참고 {#section-6b41a900b0ce4a9590e5861e3c81599c}

표현식 문자열에는 리터럴 &lt; 및 문자를 사용할 수 없습니다. 이러한 예약된 문자는 각각 `&` 및 `<` 로 인코딩하거나 전체 문자열을 XML `CDATA` 섹션에 묶을 수 있습니다.

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>` 및 `</expression>` 태그 사이의 모든 문자가 선택적 `CDATA` 섹션 외부의 문자를 포함하여 일반 표현식 구문 분석기에 전달됩니다. 추가 공백을 방지하려면 주의해야 합니다.

## 참조 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
