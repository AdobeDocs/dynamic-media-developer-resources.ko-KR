---
description: 이미지 렌더링 구성 설정은  [!DNL Platform Server] 구성 파일에 저장됩니다.
solution: Experience Manager
title: 구성 파일
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 구성 파일{#configuration-files}

이미지 렌더링 구성 설정은 [!DNL Platform Server] 구성 파일에 저장됩니다.

플랫폼 서버 구성 파일은 [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]에 있습니다. 이 파일은 JAVA 속성 파일입니다. 적절한 규칙을 따르도록 주의해야 합니다. 그렇지 않으면 [!DNL Platform Server]을(를) 시작하지 못할 수 있습니다. Windows 파일 경로에서는 단순 백슬래시(\) 대신 이중 백슬래시(`\\`) 또는 단일 슬래시(/)를 사용해야 합니다. 백슬래시가 이러한 유형의 파일에서 이스케이프 문자로 사용되기 때문입니다. 파일에 내부 서버 용이며 수정해서는 안 되는 문서화되지 않은 속성이 있습니다.

모든 이미지 렌더링 구성 설정 목록은 [구성 설정 참조](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81)를 참조하십시오.
