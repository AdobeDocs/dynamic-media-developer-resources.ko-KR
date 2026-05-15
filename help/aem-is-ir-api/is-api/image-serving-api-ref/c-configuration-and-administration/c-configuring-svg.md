---
description: SvgRender 구성 요소는 독립 Java 애플리케이션입니다.
solution: Experience Manager
title: SVG 구성
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
TQID: 'https://experienceleague.adobe.com/e6eoh1OQJoWFv0-C1xQTqygrGY4Z7m6IkefFblj-yuE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 3%

---

# SVG 구성{#configuring-svg}

SvgRender 구성 요소는 독립 Java 애플리케이션입니다.

SVG 구성 설정은 [!DNL PlatformServer.conf], [!DNL SVG.conf], [!DNL ImageServerRegistry.xml] 및 [!DNL ServerSupervisorRegistry.xml]에 있습니다.

소켓 연결은 SvgRender와 이미지 서버 간의 통신에 사용됩니다. 포트 번호가 27346. 필요한 경우 [!DNL svg.conf]의 `SVGRender.port` 및 [!DNL ImageServerRegistry.xml]의 `<SVGTcpPort>`을(를) 새 값으로 설정하여 변경할 수 있습니다.

## 참조 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG 구성 설정](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
