---
description: 이미지 렌더링은 피라미드가 아닌 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.
seo-description: 이미지 렌더링은 피라미드가 아닌 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.
seo-title: 비네팅 크기 제한
solution: Experience Manager
title: 비네팅 크기 제한
topic: Scene7 Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 비네팅 크기 제한{#vignette-size-limitation}

이미지 렌더링은 피라미드가 아닌 비네팅에 대해 2메가픽셀 크기 제한을 적용합니다.

응용 프로그램에서 이 `IrMaxNonPyrVignetteSize` 제한보다 큰 이미지 영역(너비 x 높이)을 가진 비피라미드형 비네팅을 지원해야 하는 경우 [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]의 값을 수정합니다.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>`attribute::MaxPix` 또한 비정상적으로 큰 응답 이미지 크기를 허용하도록 조정해야 `IS::MaxMessageSize` 할 수도 있습니다. 자세한 내용은 이미지 제공 설명서를 참조하십시오.

