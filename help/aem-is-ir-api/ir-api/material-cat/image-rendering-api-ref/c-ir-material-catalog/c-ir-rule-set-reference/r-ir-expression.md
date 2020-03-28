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

---


# 식{#expression}

정규 표현식 패턴 요소입니다. 선택 `<rule>` 사항입니다.

## 속성 {#section-fd0574eee1f9423cbb2ed709c0906800}

없음.

## 데이터 {#section-4cd740c511a1432da0955e9acfbcf96f}

정규 표현식 패턴 문자열.

## 설명 {#section-3245c8a531bb455d8398449f6ea63b37}

요소는 비어 있거나 단순 검색 문자열이나 정규 표현식 패턴을 포함할 수 `<expression>` 있습니다. 패턴은 전체 요청 문자열에 적용됩니다.

검색은 항상 비어 있거나 지정되지 `<expression>` 않았을 때 발생합니다.이는 지정하는 것과 `<expression>.*</expression>`같습니다.

이 구현은 Perl과 유사한 정규 표현식 구문을 제공하는 [java 패키지](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)java.util.regex를 기반으로 합니다.

## 참고 {#section-6b41a900b0ce4a9590e5861e3c81599c}

표현식 문자열에는 리터럴 &lt; 및 &amp; 문자가 포함될 수 없습니다. 이러한 예약 문자는 각각 `&` 및 `<`로 인코딩하거나 전체 문자열을 XML `CDATA` 섹션으로 묶을 수 있습니다.

`<expression><![CDATA[&fmt=custom]]></expression>`

옵션 `<expression>` `</expression>` `CDATA` 섹션 외부의 문자를 포함하여 태그와 태그 사이의 모든 문자가 정규 표현식 파서로 전달됩니다. 공백은 피하도록 주의해야 한다.

## 참조 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
