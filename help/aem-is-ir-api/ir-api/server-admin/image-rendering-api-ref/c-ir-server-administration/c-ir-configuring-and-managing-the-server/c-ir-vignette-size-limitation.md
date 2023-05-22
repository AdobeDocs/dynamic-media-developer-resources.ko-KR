---
description: 이미지 렌더링은 비피라미드 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.
solution: Experience Manager
title: 비네팅 크기 제한
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# 비네팅 크기 제한{#vignette-size-limitation}

이미지 렌더링은 비피라미드 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.

값 수정 `IrMaxNonPyrVignetteSize` [!DNL]에서 *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] 응용 프로그램에서 이 제한보다 큰 이미지 영역(너비 x 높이)의 비피라미드 비네팅을 지원해야 하는 경우

>[!NOTE]
>
>`attribute::MaxPix` 및 `IS::MaxMessageSize` 비정상적으로 큰 응답 이미지 크기를 허용하도록 조정되어야 할 수도 있습니다. 자세한 내용은 이미지 제공 설명서 를 참조하십시오.
