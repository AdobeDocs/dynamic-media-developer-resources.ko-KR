---
description: 검색 결과에서 제외할 생성 엔진 및 생성된 자산 유형을 결정합니다.
solution: Experience Manager
title: 제외 부산물 조건
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 9%

---


# ExcludeMozineCondition{#excludebyproductcondition}

검색 결과에서 제외할 생성 엔진 및 생성된 자산 유형을 결정합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`엔진`*` | `xsd:string` | 제외할 자산을 만든 생성 엔진. 값은 생성 정보를 참조하십시오. |
| `*`generatedAssetType`*` | `xsd:string` | 제외된 자산 유형. 값에 대해서는 자산 유형을 참조하십시오. |

