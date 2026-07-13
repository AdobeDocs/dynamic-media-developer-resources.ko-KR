---
title: 비네팅 크기 제한
description: 이미지 렌더링은 비피라미드 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
TQID: 'https://experienceleague.adobe.com/qPrnkvYXinvZAfx-s6ePjpe64qsoBfwtVbUJ-fYBbmc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 0%

---

# 비네팅 크기 제한{#vignette-size-limitation}

이미지 렌더링은 비피라미드 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.

응용 프로그램에서 이미지 영역(너비 x 높이)이 이 제한보다 큰 비피라미드 비네팅을 지원하려면 [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]에서 `IrMaxNonPyrVignetteSize` 값을 수정합니다.

>[!NOTE]
>
>응답 이미지 크기가 비정상적으로 크도록 `attribute::MaxPix` 및 `IS::MaxMessageSize` 특성을 조정하십시오. 자세한 내용은 이미지 제공 설명서 를 참조하십시오.

