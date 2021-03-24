---
description: 대체 문자열 요소입니다. <rule> 요소의 선택 사항입니다.
solution: Experience Manager
title: 대체
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# 대체{#substitution}

대체 문자열 요소입니다. `<rule>` 요소의 선택 사항입니다.

## 속성 {#section-a4506fcb765f4f128f7f1f2629b18a6c}

없음.

## 데이터 {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

대체 문자열.

## 설명 {#section-4a64a93f5e1a4d04a2db19166578bf76}

경로 또는 쿼리에서 일치하는 문자열 또는 하위 문자열에 대한 대체 문자열을 정의합니다.

패턴 표현식에 하위 표현식(괄호로 구분됨)이 포함되어 있으면 첫 번째 일치하는 하위 문자열이 대체 문자열로 대체됩니다. 패턴 식에 하위 표현식이 포함되지 않으면 일치하는 문자열 전체가 대체됩니다.

`<expression>`이(가) 비어 있거나 없는 경우 대체 문자열이 경로나 쿼리에 추가됩니다.

`<substitution>`이(가) 비어 있으면 일치하는 문자열 또는 하위 문자열이 제거됩니다. `<substitution>`이(가) 지정되지 않은 경우 경로 또는 쿼리 문자열이 수정되지 않습니다.

>[!NOTE]
>
>입력 문자열의 모든 일치 항목은 `replace="all"`이(가) 이 `<substitution>` 요소가 속하는 요소에 지정된 경우 대체됩니다. `<rule>` 기본적으로 첫 번째 일치만 대체 문자열로 대체됩니다.

## 참고 {#section-cedf2adabaaf441c9f598fb0ea180246}

대체 문자열에는 리터럴 &lt; 및 &amp; 문자가 포함될 수 없습니다. 이러한 예약된 문자는 각각 `&` 및 `<`로 인코딩할 수 있고, 전체 문자열을 XML CDATA 섹션에 포함할 수 있습니다.

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
