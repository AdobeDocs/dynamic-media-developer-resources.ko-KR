---
description: 대체 문자열 요소입니다. <rule> 요소의 선택 사항입니다.
seo-description: 대체 문자열 요소입니다. <rule> 요소의 선택 사항입니다.
seo-title: 대체
solution: Experience Manager
title: 대체
topic: Scene7 Image Serving - Image Rendering API
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---


# 대체{#substitution}

대체 문자열 요소입니다. `<rule>` 요소의 선택 사항입니다.

## 속성 {#section-d955eefc53eb4274861270669c01f9ca}

없음.

## 데이터 {#section-a2688866ed6d41279a8478886e511ae3}

대체 문자열.

## 설명 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

경로 또는 쿼리에서 일치하는 문자열 또는 하위 문자열에 대한 대체 문자열을 정의합니다.

패턴 표현식에 하위 표현식(괄호로 구분됨)이 포함되어 있으면 첫 번째 일치 하위 문자열이 대체 문자열로 대체됩니다. 패턴 식에 하위 표현식이 포함되지 않으면 일치하는 문자열 전체가 대체됩니다.

`<expression>`이(가) 비어 있거나 없는 경우 대체 문자열이 경로나 쿼리에 추가됩니다.

`<substitution>`이(가) 비어 있으면 일치하는 문자열 또는 하위 문자열이 제거됩니다. `<substitution>`이(가) 지정되지 않은 경우 경로 또는 쿼리 문자열이 수정되지 않습니다.

## 참고 {#section-90fe89bb17a04804b7ff3c93df082892}

대체 문자열에는 리터럴 &lt; 및 &amp; 문자가 포함될 수 없습니다. 이러한 예약된 문자는 각각 `&` 및 `<`로 인코딩할 수 있고, 전체 문자열을 XML `CDATA` 섹션에 포함할 수 있습니다.

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
