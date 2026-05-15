---
description: 정규 표현식 패턴 요소입니다. <rule> 요소에서 선택 사항입니다.
solution: Experience Manager
title: 표현식
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
TQID: 'https://experienceleague.adobe.com/zMAFfzeypXmMIx1aO1xmHdF-UkHJPHKp7KUgi05F94w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 2%

---

# 표현식{#expression}

정규 표현식 패턴 요소입니다. `<rule>` 요소에서 선택 사항입니다.

## 속성 {#section-fd0574eee1f9423cbb2ed709c0906800}

없음.

## 데이터 {#section-4cd740c511a1432da0955e9acfbcf96f}

정규 표현식 패턴 문자열입니다.

## 설명 {#section-3245c8a531bb455d8398449f6ea63b37}

`<expression>` 요소는 비어 있거나 단순 검색 문자열 또는 정규 표현식 패턴을 포함할 수 있습니다. 패턴은 전체 요청 문자열에 적용됩니다.

`<expression>`이(가) 비어 있거나 지정되지 않은 경우 항상 일치가 발생합니다. 이는 `<expression>.*</expression>`을(를) 지정하는 것과 같습니다.

구현은 Perl과 유사한 정규 표현식 구문을 제공하는 Java 패키지 [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e)을(를) 기반으로 합니다.

## 참고 {#section-6b41a900b0ce4a9590e5861e3c81599c}

표현식 문자열에는 리터럴 &lt; 및 &amp; 문자를 사용할 수 없습니다. 예약된 이러한 문자는 각각 `&` 및 `<`(으)로 인코딩하거나 전체 문자열을 XML `CDATA` 섹션에 포함할 수 있습니다.

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`과(와) `</expression>` 태그 사이의 모든 문자는 선택적 `CDATA` 섹션 외부의 문자를 포함하여 정규식 파서로 전달됩니다. 여분의 공백을 피하기 위해 주의해야 합니다.

## 참조 {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
