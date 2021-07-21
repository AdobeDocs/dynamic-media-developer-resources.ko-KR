---
description: SvgRender 구성 요소는 독립 Java 응용 프로그램입니다.
solution: Experience Manager
title: SVG 구성
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# SVG 구성{#configuring-svg}

SvgRender 구성 요소는 독립 Java 응용 프로그램입니다.

SVG 구성 설정은 [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] 및 [!DNL ServerSupervisorRegistry.xml]에 있습니다.

소켓 연결은 SvgRender와 이미지 서버 간에 통신하는 데 사용됩니다. 포트 번호는 27346. 필요한 경우 [!DNL svg.conf]에서 `SVGRender.port`, [!DNL ImageServerRegistry.xml]에서 `<SVGTcpPort>`를 새 값으로 설정하여 변경할 수 있습니다.

## 참조 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG 구성 설정](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
