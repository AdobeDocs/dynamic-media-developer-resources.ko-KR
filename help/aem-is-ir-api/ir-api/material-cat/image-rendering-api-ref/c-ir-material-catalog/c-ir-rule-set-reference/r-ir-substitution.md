---
title: 대체
description: 대체 문자열 요소입니다. <rule> 요소에서 선택 사항입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
TQID: 'https://experienceleague.adobe.com/GqJBLso7oigoeCJ-0KQzFv2aeoAiVzumjlDTtjBSDI4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 1%

---

# 대체{#substitution}

대체 문자열 요소입니다. `<rule>` 요소에서 선택 사항입니다.

## 속성 {#section-d955eefc53eb4274861270669c01f9ca}

없음.

## 데이터 {#section-a2688866ed6d41279a8478886e511ae3}

대체 문자열.

## 설명 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

경로 또는 쿼리에서 일치하는 문자열 또는 하위 문자열에 대한 대체 문자열을 정의합니다.

패턴 표현식에 하위 표현식(괄호로 구분)이 포함된 경우 첫 번째 일치하는 하위 문자열은 대체 문자열로 대체됩니다. 패턴 표현식에 하위 표현식이 포함되지 않으면 일치하는 전체 문자열이 대체됩니다.

`<expression>`이(가) 비어 있거나 없으면 대체 문자열이 경로 또는 쿼리에 추가됩니다.

`<substitution>`이(가) 비어 있으면 일치하는 문자열 또는 하위 문자열이 제거됩니다. `<substitution>`을(를) 지정하지 않으면 경로나 쿼리 문자열이 수정되지 않습니다.

## 참고 {#section-90fe89bb17a04804b7ff3c93df082892}

대체 문자열은 리터럴 &lt; 및 &amp; 문자를 포함하지 않아야 합니다. 예약된 이러한 문자는 각각 `&` 및 `<`(으)로 인코딩하거나 전체 문자열을 XML `CDATA` 섹션에 포함할 수 있습니다.

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
