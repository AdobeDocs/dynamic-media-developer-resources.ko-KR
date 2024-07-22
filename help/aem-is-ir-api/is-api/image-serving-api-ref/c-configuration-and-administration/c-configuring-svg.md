---
description: SvgRender 구성 요소는 독립 Java 애플리케이션입니다.
solution: Experience Manager
title: 구성 SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# 구성 SVG{#configuring-svg}

SvgRender 구성 요소는 독립 Java 애플리케이션입니다.

SVG 구성 설정이 [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] 및 [!DNL ServerSupervisorRegistry.xml]에 있습니다.

소켓 연결은 SvgRender와 이미지 서버 간의 통신에 사용됩니다. 포트 번호가 27346. 필요한 경우 [!DNL svg.conf]의 `SVGRender.port` 및 [!DNL ImageServerRegistry.xml]의 `<SVGTcpPort>`을(를) 새 값으로 설정하여 변경할 수 있습니다.

## 참조 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG 구성 설정](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
