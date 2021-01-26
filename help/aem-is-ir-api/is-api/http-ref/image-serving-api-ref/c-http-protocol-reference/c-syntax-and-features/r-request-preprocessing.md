---
description: 이미지 제공은 정규 표현식 일치 및 대체 규칙에 따라 간단한 요청 프리프로세서를 제공합니다.
seo-description: 이미지 제공은 정규 표현식 일치 및 대체 규칙에 따라 간단한 요청 프리프로세서를 제공합니다.
seo-title: 사전 처리 요청
solution: Experience Manager
title: 사전 처리 요청
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# 사전 처리 요청{#request-preprocessing}

이미지 제공은 정규 표현식 일치 및 대체 규칙에 따라 간단한 요청 프리프로세서를 제공합니다.

규칙 컬렉션(규칙 세트)은 기본 카탈로그를 포함하여 각 이미지 카탈로그에 첨부할 수 있습니다. 규칙은 XML 형식 파일로 지정됩니다.

요청 전처리 규칙은 경로를 조작하고, 명령을 추가하고, 명령 값을 변경하고, 템플릿이나 매크로 적용을 포함하여, 플랫폼 서버의 파서에서 처리하기 전에 요청의 경로와 쿼리 부분을 수정할 수 있습니다. 또한 규칙을 사용하여 요청 난독화, 워터마크 등의 카탈로그 특성으로만 일반적으로 제어되는 특정 보안 기능을 구성하고 재정의하거나 특정 클라이언트 IP 주소로 HTTP 서비스를 제한하는 데 사용할 수 있습니다.

요청 사전 처리 규칙은 다양한 응용 프로그램에 적합하며, 그 중 일부는 아래에 나열되어 있습니다.

* 요청 경로를 파일, FTP 및 HTTP 경로에 다시 매핑하도록 허용하는 *가상 경로* 메커니즘을 구현합니다.
* 워터마크 등의 보안 기능을 선택적으로 적용하여 이미지 이름 또는 경로로 필터링합니다.
* 특정 IP 주소에서 서버에 액세스할 때 워터마크 또는 기타 보안 기능 생략
* `defaultImage=` 등의 명령을 모든 요청이나 URL 경로나 쿼리 문자열에 특정 패턴이 나타나는 요청에 강제 적용합니다.
* 서버 남용을 방지하기 위해 CPU 중심 명령 사용을 허용하지 않습니다.
* 소스 이미지가 `src=`이 아닌 요청 경로에서 소스 이미지를 지정하면서 HTTP 또는 FTP 서버에 위치하도록 허용합니다.
* 요청 경로나 이미지 이름에 따라 이미지 품질 설정(예: JPEG 품질 또는 선명하게 하기)을 제어합니다.

규칙 세트 만들기, 사용 및 관리에 대한 자세한 내용은 [규칙 세트 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)에서 확인할 수 있습니다.

## 참조 {#see-also}

[규칙 세트 참조](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [특성::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
