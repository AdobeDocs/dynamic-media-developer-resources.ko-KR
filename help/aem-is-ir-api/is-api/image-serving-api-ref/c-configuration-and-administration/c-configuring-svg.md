---
description: SvgRender 구성 요소는 독립적인 Java 애플리케이션입니다.
solution: Experience Manager
title: SVG 구성
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 2%

---


# SVG{#configuring-svg} 구성

SvgRender 구성 요소는 독립적인 Java 애플리케이션입니다.

SVG 구성 설정은 [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] 및 [!DNL ServerSupervisorRegistry.xml]에 있습니다.

소켓 연결은 SvgRender와 이미지 서버 간에 통신하는 데 사용됩니다. 포트 번호는 27346입니다. 필요한 경우 [!DNL svg.conf]의 `SVGRender.port` 및 [!DNL ImageServerRegistry.xml]의 `<SVGTcpPort>`를 새 값으로 설정하여 변경할 수 있습니다.

## 참조 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG 구성 설정](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
