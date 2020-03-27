---
description: 작업이 실행된 후 작업 로그.
seo-description: 작업이 실행된 후 작업 로그.
seo-title: 작업 로그
solution: Experience Manager
title: 작업 로그
topic: Scene7 Image Production System API
uuid: d267009a-e4ad-4a21-ae0e-caf51d2f338b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 작업 로그{#joblog}

작업이 실행된 후 작업 로그.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 회사 핸들 |
| ` *`jobHandle`*` | `xsd:string` | 작업 핸들 |
| ` *`jobName`*` | `xsd:string` | 작업 이름. |
| ` *`originalJobName`*` | `xsd:string` | 작업에 대해 제출된 원래 이름입니다 `submitJob`. |
| ` *`submitUserEmail`*` | `xsd:string` | 작업을 제출한 사용자의 이메일 주소입니다. |
| ` *`logType`*` | `xsd:string` | 작업 로그 유형 선택 |
| ` *`jobSubType`*` | `xsd:string` | 추가 작업 정보. |
| ` *`startDate`*` | `xsd:dateTime` | 작업의 시작 날짜, 시간 및 표준 시간대 |
| ` *`endDate`*` | `xsd:dateTime` | 작업의 종료 날짜, 시간 및 시간대입니다. |
| ` *`description`*` | `xsd:string` | 에 원래 지정된 작업에 대한 `submitJob`설명입니다. |
| ` *`fileSuccessCount`*` | `xsd:int` | 성공적으로 처리된 파일 수입니다. |
| ` *`fileErrorCount`*` | `xsd:int` | 오류를 일으킨 파일 수입니다. |
| ` *`fileWarningCount`*` | `xsd:int` | 경고를 생성한 파일 수입니다. |
| ` *`fileDuplicateCount`*` | `xsd:int` | 중복된 파일 수입니다. |
| ` *`fileUpdateCount`*` | `xsd:int` | 업데이트된 파일 수입니다. |
| ` *`totalFileCount`*` | `xsd:int` | 기록된 작업에서 처리한 파일 수입니다. |
| ` *`transferSuccessCount`*` | `xsd:int` | 성공한 전송 수입니다. |
| ` *`transferErrorCount`*` | `xsd:int` | 전송 오류 수입니다. |
| ` *`transferWarningCount`*` | `xsd:int` | 전송 경고 수입니다. |
| ` *`fatalError`*` | `xsd:boolean` | 작업에서 치명적인 오류를 생성했는지 여부. |
| ` *`detailTotalRows`*` | `xsd:int` | 쿼리와 일치하는 총 행 수입니다. 페이지 크기 제한으로 `detailArray` 인해 크기보다 클 수 있습니다. |
| ` *`detailArray`*` | `types:JobLogDetailArray` | 기록된 작업에 대한 세부 정보 배열입니다. |

