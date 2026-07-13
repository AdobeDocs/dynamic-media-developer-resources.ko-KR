---
description: 에셋 또는 폴더의 디스크 공간 통계입니다.
solution: Experience Manager
title: 디스크 사용량
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
TQID: 'https://experienceleague.adobe.com/Md0oAgpJDqSrn1JRZsebpaZKeXIAoLcgkC5KPaHad5s'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 50
ht-degree: 10%

---

# [!DNL DiskUsage]{#diskusage}

에셋 또는 폴더의 디스크 공간 통계입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| company핸들 | `xsd:string` | 회사 핸들. |
| companyName | `xsd:string` | 회사 이름. |
| imageCount | `xsd:int` | 저장된 이미지 수. |
| 디스크 공간 사용 | `xsd:long` | 총 파일 면(KB)입니다. |
| 마지막 수정일 | `xsd:dateTime` | `DiskUsage` 유형을 마지막으로 수정한 날짜, 시간 및 시간대입니다. |

