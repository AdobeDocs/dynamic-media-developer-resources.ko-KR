---
description: 작업이 실행된 후 작업 로그입니다.
solution: Experience Manager
title: 작업 로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 3%

---

# 작업 로그{#joblog}

작업이 실행된 후 작업 로그입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 회사 핸들. |
| `*`jobHandle`*` | `xsd:string` | 작업 핸들. |
| `*`jobName`*` | `xsd:string` | 작업 이름. |
| `*`originalJobName`*` | `xsd:string` | `submitJob` 작업에 대해 제출된 원래 이름입니다. |
| `*`submitUserEmail`*` | `xsd:string` | 작업을 제출한 사용자의 전자 메일 주소입니다. |
| `*`logType`*` | `xsd:string` | 작업 로그 유형 선택 |
| `*`jobSubType`*` | `xsd:string` | 추가 작업 정보입니다. |
| `*`startDate`*` | `xsd:dateTime` | 작업의 시작 날짜, 시간 및 시간대입니다. |
| `*`endDate`*` | `xsd:dateTime` | 작업의 종료 날짜, 시간 및 시간대입니다. |
| `*`설명`*` | `xsd:string` | 원래 `submitJob`에 지정된 작업에 대한 설명입니다. |
| `*`fileSuccessCount`*` | `xsd:int` | 성공적으로 처리된 파일 수입니다. |
| `*`fileErrorCount`*` | `xsd:int` | 오류를 일으킨 파일 수입니다. |
| `*`fileWarningCount`*` | `xsd:int` | 경고를 생성한 파일 수입니다. |
| `*`fileDuplicateCount`*` | `xsd:int` | 중복된 파일 수입니다. |
| `*`fileUpdateCount`*` | `xsd:int` | 업데이트된 파일 수입니다. |
| `*`totalFileCount`*` | `xsd:int` | 로그된 작업에서 처리한 파일 수입니다. |
| `*`transferSuccessCount`*` | `xsd:int` | 전송 성공 수입니다. |
| `*`transferErrorCount`*` | `xsd:int` | 전송 오류 수입니다. |
| `*`transferWarningCount`*` | `xsd:int` | 전송 경고 수입니다. |
| `*`fatalError`*` | `xsd:boolean` | 작업에서 치명적인 오류를 생성했는지 여부. |
| `*`detailTotalRows`*` | `xsd:int` | 페이지 크기 제한으로 인해 `detailArray` 크기보다 클 수 있는 쿼리와 일치하는 총 행 수입니다. |
| `*`detailArray`*` | `types:JobLogDetailArray` | 로그된 작업에 대한 세부 정보의 배열입니다. |
