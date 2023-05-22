---
description: 에셋에 대해 요약된 정보가 포함된 메타데이터 검색 결과.
solution: Experience Manager
title: 자산 요약
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# [!DNL AssetSummary]{#assetsummary}

에셋에 대해 요약된 정보가 포함된 메타데이터 검색 결과.

구문

## 매개 변수 {#section-ebc75cc024d94c439260d2e71873cc74}

| 이름 | 유형 | 설명 |
|---|---|---|
| assetHandle | `xsd:string` | 에셋 핸들. |
| 유형 | `xsd:string` | 자산 유형. 에셋 유형 상수는 가능한 값을 정의합니다. 선택적. |
| name | `xsd:string` | 에셋 이름. 선택적. |
| 폴더 | `xsd:string` | 에셋이 포함된 폴더입니다. |
| 파일 이름 | `xsd:string` | 에셋의 파일 이름입니다. |
| 생성됨 | `xsd:dateTime` | 에셋 생성일. |
| createUser | `xsd:string` | 에셋을 만든 사용자입니다. |
| 마지막 수정일 | `xsd:dateTime` | 에셋이 마지막으로 업데이트된 날짜입니다. |
| lastModifyUser | `xsd:string` | 에셋을 수정한 마지막 사용자입니다. |
| metadataArray | `types:MetadataArray` | 자산과 연결된 메타데이터 값의 배열입니다. |
| 점수 | `xsd:double` | 유사성 검색의 경우 정밀도를 정의합니다(0 = 일치 없음, 1 = 정확한 일치). |
| scoreDetail | `xsd:string` | 유사성 검색의 결과로 유사한 영역에 대한 세부 정보를 보유합니다. |
