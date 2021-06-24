---
description: 이미지 렌더링은 정규 표현식 일치 및 대체 규칙을 기반으로 간단한 요청 사전 프로세서를 제공합니다.
solution: Experience Manager
title: 사전 처리 요청 *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# 사전 처리 요청 *{#request-pre-processing}

이미지 렌더링은 정규 표현식 일치 및 대체 규칙을 기반으로 간단한 요청 사전 프로세서를 제공합니다.

규칙 모음(규칙 세트)은 기본 카탈로그를 포함하여 각 자재 카탈로그에 첨부할 수 있습니다. 규칙은 XML 형식 파일로 지정됩니다.

요청 사전 처리 규칙은 경로 조작, 명령 추가, 명령 값 변경, 템플릿 또는 매크로 적용 등 이미지 렌더링 파서가 처리하기 전에 요청의 경로와 쿼리 부분을 수정할 수 있습니다. 규칙은 기본 회신 이미지 크기 설정 또는 특정 클라이언트 IP 주소로 HTTP 서비스를 제한하는 등의 카탈로그 속성으로만 정상적으로 제어되는 특정 기능을 구성하고 재정의하는 데 사용할 수도 있습니다.

요청 사전 처리 규칙은 다양한 애플리케이션에 적합하며 일부는 아래에 나열됩니다.

* 요청 경로를 파일, FTP 및 HTTP 경로에 다시 매핑할 수 있는 *가상 경로* 메커니즘을 구현합니다.
* 서버 남용을 방지하기 위해 CPU 집약적 명령을 사용할 수 없습니다.
* 요청 경로나 이미지 이름에 따라 이미지 품질 설정(예: JPEG 품질 또는 선명하게 하기)을 제어합니다.

규칙 세트 생성, 사용 및 관리에 대한 자세한 내용은 규칙 세트 참조에서 확인할 수 있습니다.

규칙 세트 참조, attribute::RuleSetFile 도 참조하십시오.
