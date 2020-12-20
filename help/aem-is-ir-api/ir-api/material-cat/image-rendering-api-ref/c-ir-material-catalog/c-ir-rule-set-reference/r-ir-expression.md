---
description: 정규 표현식 패턴 요소입니다. <rule> 요소의 선택 사항입니다.
seo-description: 정규 표현식 패턴 요소입니다. <rule> 요소의 선택 사항입니다.
seo-title: 식
solution: Experience Manager
title: 식
topic: Scene7 Image Serving - Image Rendering API
uuid: e7ef3769-0090-42d6-8021-1c213f1ee391
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 4%

---


# 식{#expression}

정규 표현식 패턴 요소입니다. `<rule>` 요소의 선택 사항입니다.

## 속성 {#section-fd0574eee1f9423cbb2ed709c0906800}

없음.

## 데이터 {#section-4cd740c511a1432da0955e9acfbcf96f}

정규 표현식 패턴 문자열.

## 설명 {#section-3245c8a531bb455d8398449f6ea63b37}

`<expression>` 요소는 비어 있거나 단순 검색 문자열 또는 정규 표현식 패턴을 포함할 수 있습니다. 패턴은 전체 요청 문자열에 적용됩니다.

`<expression>`이(가) 비어 있거나 지정되지 않았을 때 항상 일치 항목이 발생합니다.이것은 `<expression>.*</expression>` 지정에 해당합니다.

구현은 Perl과 유사한 정규 표현식 구문을 제공하는 Java 패키지 [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)을 기반으로 합니다.

## 참고 {#section-6b41a900b0ce4a9590e5861e3c81599c}

표현식 문자열에는 리터럴 &lt; 및 &amp; 문자가 포함될 수 없습니다. 이러한 예약된 문자는 각각 `&` 및 `<`로 인코딩할 수 있고, 전체 문자열을 XML `CDATA` 섹션에 포함할 수 있습니다.

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`과 `</expression>` 태그 사이의 모든 문자는 선택적 `CDATA` 섹션 외부의 문자를 포함하여 일반 표현식 파서에 전달됩니다. 추가 공백이 없도록 주의하십시오.

## 참조 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
