---
description: 작업이 실행된 후 작업 로그입니다.
solution: Experience Manager
title: 작업 로그
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# [!DNL JobLog]{#joblog}

작업이 실행된 후 작업 로그입니다.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| company핸들 | `xsd:string` | 회사 핸들. |
| jobHandle | `xsd:string` | 작업 핸들. |
| jobName | `xsd:string` | 작업 이름. |
| originalJobName | `xsd:string` | `submitJob`(으)로 작업에 대해 원래 이름이 제출되었습니다. |
| submitUseremail | `xsd:string` | 작업을 제출한 사용자의 이메일 주소입니다. |
| logType | `xsd:string` | 작업 로그 유형 선택. |
| jobSubtype | `xsd:string` | 추가 작업 정보. |
| startDate | `xsd:dateTime` | 작업의 시작 날짜, 시간 및 시간대입니다. |
| endDate | `xsd:dateTime` | 작업의 종료 날짜, 시간 및 시간대입니다. |
| [!DNL description] | `xsd:string` | 원래 `submitJob`에 지정된 작업에 대한 설명입니다. |
| fileSuccessCount | `xsd:int` | 정상적으로 처리된 파일 수. |
| 파일 오류 수 | `xsd:int` | 오류가 발생한 파일 수입니다. |
| fileAlertCount | `xsd:int` | 경고를 생성한 파일 수입니다. |
| fileDuplicationCount | `xsd:int` | 중복 파일 수. |
| fileUpdateCount | `xsd:int` | 업데이트된 파일 수. |
| 총 파일 수 | `xsd:int` | 기록된 작업에서 처리된 파일 수입니다. |
| transferSuccessCount | `xsd:int` | 성공한 전송 수입니다. |
| transfer오류 수 | `xsd:int` | 전송 오류 수. |
| transferWarningCount | `xsd:int` | 전송 경고 수. |
| fatalError | `xsd:boolean` | 작업에서 치명적인 오류가 생성되었는지 여부입니다. |
| 세부 정보 합계 행 | `xsd:int` | 쿼리와 일치하는 총 행 수입니다. 페이지 크기 제한으로 인해 크기가 `detailArray`보다 클 수 있습니다. |
| detailArray | `types:JobLogDetailArray` | 로그된 작업에 대한 세부 정보 배열. |
