---
description: 작업이 실행된 후 작업 로그.
solution: Experience Manager
title: 작업 로그
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 3%

---


# 작업 로그{#joblog}

작업이 실행된 후 작업 로그.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 회사 핸들. |
| `*`jobHandle`*` | `xsd:string` | 작업 핸들. |
| `*`jobName`*` | `xsd:string` | 작업 이름. |
| `*`originalJobName`*` | `xsd:string` | `submitJob`이(가) 있는 작업에 대해 제출된 원래 이름입니다. |
| `*`submitUserEmail`*` | `xsd:string` | 작업을 제출한 사용자의 이메일 주소입니다. |
| `*`logType`*` | `xsd:string` | 작업 로그 유형 선택 |
| `*`jobSubType`*` | `xsd:string` | 추가 작업 정보. |
| `*`startDate`*` | `xsd:dateTime` | 작업의 시작 날짜, 시간 및 표준 시간대 |
| `*`endDate`*` | `xsd:dateTime` | 작업의 종료 날짜, 시간 및 시간대입니다. |
| `*`description`*` | `xsd:string` | `submitJob`에 원래 지정된 작업에 대한 설명입니다. |
| `*`fileSuccessCount`*` | `xsd:int` | 처리된 파일 수입니다. |
| `*`fileErrorCount`*` | `xsd:int` | 오류가 발생한 파일 수입니다. |
| `*`fileWarningCount`*` | `xsd:int` | 경고를 생성한 파일 수입니다. |
| `*`fileDuplicateCount`*` | `xsd:int` | 중복된 파일 수입니다. |
| `*`fileUpdateCount`*` | `xsd:int` | 업데이트된 파일 수입니다. |
| `*`totalFileCount`*` | `xsd:int` | 기록된 작업에 의해 처리된 파일 수입니다. |
| `*`transferSuccessCount`*` | `xsd:int` | 전송 성공 수입니다. |
| `*`transferErrorCount`*` | `xsd:int` | 전송 오류 수입니다. |
| `*`transferWarningCount`*` | `xsd:int` | 전송 경고 수입니다. |
| `*`fatalError`*` | `xsd:boolean` | 작업에서 치명적인 오류를 생성했는지 여부. |
| `*`detailTotalRows`*` | `xsd:int` | 페이지 크기 제한으로 인해 쿼리와 일치하는 총 행 수입니다. 이 수는 `detailArray` 크기보다 클 수 있습니다. |
| `*`detailArray`*` | `types:JobLogDetailArray` | 기록된 작업에 대한 세부 정보 배열입니다. |

