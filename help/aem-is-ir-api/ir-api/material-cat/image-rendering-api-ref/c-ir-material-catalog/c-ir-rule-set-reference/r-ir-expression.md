---
description: 정규 표현식 패턴 요소입니다. 에서 선택 사항 <rule> 요소.
solution: Experience Manager
title: 표현식
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 3%

---

# 표현식{#expression}

정규 표현식 패턴 요소입니다. 에서 선택 사항 `<rule>` 요소.

## 속성 {#section-fd0574eee1f9423cbb2ed709c0906800}

없음.

## 데이터 {#section-4cd740c511a1432da0955e9acfbcf96f}

정규 표현식 패턴 문자열입니다.

## 설명 {#section-3245c8a531bb455d8398449f6ea63b37}

다음 `<expression>` 요소는 비어 있거나 단순 검색 문자열 또는 정규 표현식 패턴을 포함할 수 있습니다. 패턴은 전체 요청 문자열에 적용됩니다.

일치는 항상 다음과 같을 때 발생합니다. `<expression>` 은(는) 비어 있거나 지정되지 않았습니다. 이것은 을 지정하는 것과 같습니다. `<expression>.*</expression>`.

구현은 Java 패키지를 기반으로 합니다 [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e): Perl과 유사한 정규 표현식 구문을 제공합니다.

## 참고 {#section-6b41a900b0ce4a9590e5861e3c81599c}

표현식 문자열에는 리터럴 &lt; 및 &amp; 문자를 사용할 수 없습니다. 예약된 이러한 문자는 `&` 및 `<`, 각각 또는 전체 문자열을 XML로 묶을 수 있습니다 `CDATA` 섹션:

`<expression><![CDATA[&fmt=custom]]></expression>`

다음 사이의 모든 문자 `<expression>` 및 `</expression>` 태그는 선택 사항 외부의 문자를 포함하여 정규 표현식 파서로 전달됩니다. `CDATA` 섹션. 여분의 공백을 피하기 위해 주의해야 합니다.

## 참조 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
