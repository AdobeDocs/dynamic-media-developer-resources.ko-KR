---
description: 이미지 렌더링 구성 설정은 Platform Server 구성 파일에 저장됩니다.
solution: Experience Manager
title: 구성 파일
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 구성 파일{#configuration-files}

이미지 렌더링 구성 설정은 Platform Server 구성 파일에 저장됩니다.

플랫폼 서버 구성 파일은 [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]에 있습니다. 이 파일은 JAVA 속성 파일입니다. 적절한 규칙을 따르려면 주의해야 합니다. 그렇지 않으면 Platform Server를 시작할 수 없습니다. 이 유형의 파일에서 백슬래시는 이스케이프 문자로 사용되므로 Windows 파일 경로에서 단순 백슬래시(\) 대신 이중 백슬래시(`\\`) 또는 단일 슬래시(/)를 사용해야 합니다. 파일에 내부 서버 사용을 위한 문서화되지 않은 속성이 포함되어 있으며 수정하면 안 됩니다.

모든 이미지 렌더링 구성 설정 목록은 [구성 설정 참조](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81)를 참조하십시오.
