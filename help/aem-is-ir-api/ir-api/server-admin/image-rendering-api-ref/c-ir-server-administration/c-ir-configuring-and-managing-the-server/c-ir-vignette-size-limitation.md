---
description: 이미지 렌더링에서는 피라미드가 아닌 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.
solution: Experience Manager
title: 비네팅 크기 제한
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# 비네팅 크기 제한{#vignette-size-limitation}

이미지 렌더링에서는 피라미드가 아닌 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.

응용 프로그램에서 이 제한보다 큰 이미지 영역(너비 x 높이)을 가진 비피라미드형 비메타데이터에 대한 지원이 필요한 경우 [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]에서 `IrMaxNonPyrVignetteSize` 값을 수정합니다.

>[!NOTE]
>
>`attribute::MaxPix` 및  `IS::MaxMessageSize` 를 조정해야 비정상적으로 큰 응답 이미지 크기를 사용할 수 있습니다. 자세한 내용은 이미지 제공 설명서 를 참조하십시오.
