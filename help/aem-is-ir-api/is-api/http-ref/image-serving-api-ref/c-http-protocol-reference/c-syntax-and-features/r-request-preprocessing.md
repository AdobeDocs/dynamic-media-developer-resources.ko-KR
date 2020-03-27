---
description: 이미지 제공은 정규 표현식 일치 및 대체 규칙에 따라 간단한 요청 프리프로세서를 제공합니다.
seo-description: 이미지 제공은 정규 표현식 일치 및 대체 규칙에 따라 간단한 요청 프리프로세서를 제공합니다.
seo-title: 사전 처리 요청
solution: Experience Manager
title: 사전 처리 요청
topic: Scene7 Image Serving - Image Rendering API
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 사전 처리 요청{#request-preprocessing}

이미지 제공은 정규 표현식 일치 및 대체 규칙에 따라 간단한 요청 프리프로세서를 제공합니다.

Collections of rules (rule sets) can be attached to each image catalog, including the default catalog. 규칙은 XML 형식 파일로 지정됩니다.

Request preprocessing rules can modify the path and query portions of requests before they are processed by the Platform Server&#39;s parser, including manipulating the path, adding commands, changing command values, and applying templates or macros. 또한 규칙을 사용하여 요청 난독화, 워터마크 등의 카탈로그 속성으로만 일반적으로 제어되는 특정 보안 기능을 구성하고 재정의하거나 특정 클라이언트 IP 주소로 HTTP 서비스를 제한하는 데 사용할 수 있습니다.

Request preprocessing rules are suitable for a variety of applications, some of which are listed below:

* 요청 경로를 파일, FTP 및 HTTP 경로에 다시 매핑할 수 있는 *가상 경로* 메커니즘을 구현합니다.
* 워터마킹과 같은 보안 기능을 선택적으로 적용하여 이미지 이름이나 경로로 필터링합니다.
* 특정 IP 주소에서 서버에 액세스할 때 워터마크 또는 기타 보안 기능 생략
* URL 경로나 쿼리 문자열에서 특정 패턴을 표시하는 요청이나 모든 요청과 같은 명령을 `defaultImage=`강제로 적용하는 행위
* 서버 남용을 방지하기 위해 CPU 중심 명령을 사용할 수 없도록 합니다.
* 소스 이미지가 HTTP 또는 FTP 서버에 위치할 수 있도록 허용하면서 요청 경로에 지정하는 대신 `src=`사용합니다.
* 요청 경로나 이미지 이름에 따라 이미지 품질 설정(예: JPEG 품질 또는 선명하게 하기)을 제어할 수 있습니다.

규칙 세트 만들기, 사용 및 관리에 대한 자세한 내용은 규칙 세트 [참조에서 확인할 수 있습니다](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## 참조 {#see-also}

[규칙 세트 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [속성::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
