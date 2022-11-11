---
description: 검색 결과에서 제외할 생성 엔진 및 생성된 자산 유형을 결정합니다.
solution: Experience Manager
title: 제외 부산물 조건
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5b37e01b-9e9c-4d34-9d39-1f9bfe356e53
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# [!DNL ExcludeByproductCondition]{#excludebyproductcondition}

검색 결과에서 제외할 생성 엔진 및 생성된 자산 유형을 결정합니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 제외할 자산을 만든 생성 엔진입니다. 값에 대해서는 생성 정보 를 참조하십시오. |
| generatedAssetType | `xsd:string` | 제외된 자산 유형. 값에 대해서는 자산 유형 을 참조하십시오. |
