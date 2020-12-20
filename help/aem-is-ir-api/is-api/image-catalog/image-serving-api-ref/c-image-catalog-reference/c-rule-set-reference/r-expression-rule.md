---
description: 정규 표현식 패턴 요소입니다. <rule> 요소의 선택 사항입니다.
seo-description: 정규 표현식 패턴 요소입니다. <rule> 요소의 선택 사항입니다.
seo-title: 식
solution: Experience Manager
title: 식
topic: Scene7 Image Serving - Image Rendering API
uuid: f2036015-a2c7-4392-86f6-4cdf3152839a
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 4%

---


# 식{#expression}

정규 표현식 패턴 요소입니다. `<rule>` 요소의 선택 사항입니다.

## 속성 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

없음.

## 데이터 {#section-e2601008d71243109af1a8c55b58416d}

정규 표현식 패턴 문자열.

## 설명 {#section-759bfb738ddb45dba1f0807aba8c1113}

`<expression>` 요소는 비어 있거나 단순 검색 문자열 또는 정규 표현식 패턴을 포함할 수 있습니다. 패턴은 전체 요청 문자열에 적용됩니다.

`<expression>`이(가) 비어 있거나 지정되지 않았을 때 항상 일치 항목이 발생합니다.이것은 `<expression>.*</expression>` 지정에 해당합니다.

구현은 Perl과 유사한 정규 표현식 구문을 제공하는 Java 패키지 [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)을 기반으로 합니다.

## 주의 {#section-10b472a902674893b49ca49a7052c366}

표현식 문자열에는 리터럴 &lt; 및 &amp; 문자가 포함될 수 없습니다. 이러한 예약된 문자는 각각 `&` 및 `<`로 인코딩할 수 있고, 전체 문자열을 XML `CDATA` 섹션에 포함할 수 있습니다.

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`과 `</expression>` 태그 사이의 모든 문자는 선택적 `CDATA` 섹션 외부의 문자를 포함하여 일반 표현식 파서에 전달됩니다. 추가 공백이 없도록 주의하십시오.

## 참조 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
