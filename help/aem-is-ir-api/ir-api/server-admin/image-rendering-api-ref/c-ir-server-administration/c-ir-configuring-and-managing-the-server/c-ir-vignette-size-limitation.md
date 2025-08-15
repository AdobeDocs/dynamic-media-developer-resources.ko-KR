---
title: 비네팅 크기 제한
description: 이미지 렌더링은 비피라미드 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# 비네팅 크기 제한{#vignette-size-limitation}

이미지 렌더링은 비피라미드 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.

응용 프로그램에서 이미지 영역(너비 x 높이)이 이 제한보다 큰 비피라미드 비네팅을 지원하려면 [!DNL `IrMaxNonPyrVignetteSize` /ImageServing/conf /ImageServerRegistry.conf]에서 *[!DNL install_root]* 값을 수정합니다.

>[!NOTE]
>
>응답 이미지 크기가 비정상적으로 크도록 `attribute::MaxPix` 및 `IS::MaxMessageSize` 특성을 조정하십시오. 자세한 내용은 이미지 제공 설명서 를 참조하십시오.
