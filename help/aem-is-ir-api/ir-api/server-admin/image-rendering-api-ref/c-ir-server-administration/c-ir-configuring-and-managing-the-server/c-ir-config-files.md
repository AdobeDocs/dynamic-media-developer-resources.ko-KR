---
description: 이미지 렌더링 구성 설정은 플랫폼 서버 구성 파일에 저장됩니다.
seo-description: 이미지 렌더링 구성 설정은 플랫폼 서버 구성 파일에 저장됩니다.
seo-title: 구성 파일
solution: Experience Manager
title: 구성 파일
topic: Scene7 Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# 구성 파일{#configuration-files}

이미지 렌더링 구성 설정은 플랫폼 서버 구성 파일에 저장됩니다.

플랫폼 서버 구성 파일은 [!DNL /ImageServing/conf/PlatformServer.conf]에 *[!DNL install_root]*&#x200B;있습니다. 이 파일은 JAVA 속성 파일입니다. 적절한 규칙을 따르도록 주의해야 합니다. 그렇지 않으면 플랫폼 서버를 시작할 수 없습니다. 백슬래시는 이 유형의 파일에서 이스케이프 문자로 사용되므로 Windows 파일 경로에서 단순 백슬래시(\) 대신 이중 백슬래시(`\\`) 또는 단일 슬래시(/)를 사용해야 합니다. 파일에는 문서화되지 않은 속성이 들어 있습니다. 이 속성은 내부 서버를 사용하기 위한 것이며 수정해서는 안 됩니다.

모든 이미지 렌더링 [구성](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) 설정 목록은 구성 설정 참조를 참조하십시오.
