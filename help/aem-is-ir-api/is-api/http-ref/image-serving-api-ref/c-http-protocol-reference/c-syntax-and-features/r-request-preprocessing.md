---
description: Image Serving은 정규 표현식 일치 및 대체 규칙을 기반으로 간단한 요청 사전 프로세서를 제공합니다.
solution: Experience Manager
title: 사전 처리 요청
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 사전 처리 요청{#request-preprocessing}

Image Serving은 정규 표현식 일치 및 대체 규칙을 기반으로 간단한 요청 사전 프로세서를 제공합니다.

규칙 컬렉션(규칙 세트)은 기본 카탈로그를 포함하여 각 이미지 카탈로그에 첨부할 수 있습니다. 규칙은 XML 형식 파일로 지정됩니다.

요청 사전 처리 규칙은 경로 조작, 명령 추가, 명령 값 변경, 템플릿 또는 매크로 적용 등 Platform Server의 파서가 처리하기 전에 요청의 경로 및 쿼리 부분을 수정할 수 있습니다. 또한 규칙을 사용하여 요청 난독화, 워터마킹 등의 카탈로그 속성으로만 일반적으로 제어되는 특정 보안 기능을 구성하고 재정의할 수 있으며 HTTP 서비스를 특정 클라이언트 IP 주소로 제한할 수도 있습니다.

요청 사전 처리 규칙은 다양한 애플리케이션에 적합하며 일부는 아래에 나열됩니다.

* 요청 경로를 파일, FTP 및 HTTP 경로에 다시 매핑할 수 있는 *가상 경로* 메커니즘을 구현합니다.
* 워터마킹과 같은 보안 기능을 선택적으로 적용할 수 있습니다.
* 특정 IP 주소에서 서버에 액세스할 때 워터마크 또는 기타 보안 기능 생략
* URL 경로 또는 쿼리 문자열에서 특정 패턴을 나타내는 요청이나 모든 요청에 `defaultImage=` 등의 명령을 강제로 적용할 수 있습니다.
* 서버 남용을 방지하기 위해 CPU 집약적 명령을 사용할 수 없습니다.
* 소스 이미지를 `src=` 대신 요청 경로에서 지정하면서 HTTP 또는 FTP 서버에 배치할 수 있도록 허용합니다.
* 요청 경로나 이미지 이름에 따라 이미지 품질 설정(예: JPEG 품질 또는 선명하게 하기)을 제어합니다.

규칙 세트를 만들고, 사용하고, 관리하는 방법에 대한 자세한 내용은 [규칙 세트 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)에서 확인할 수 있습니다.

## 참조 {#see-also}

[규칙 세트 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [속성::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
