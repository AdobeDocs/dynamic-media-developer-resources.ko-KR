---
description: 점진적 JPEG 스캔 점진적 JPEG는 처음에 전체적으로 흐리거나 품질이 낮은 사진을 표시하는 방식으로 이미지를 표시합니다. 스캔이 계속 진행되면 이미지의 데이터가 더 완전히 다운로드되면 더 명확해집니다. 이 매개 변수를 사용하면 전체 이미지가 표시되도록 스캔 수(3, 4 또는 5)를 설정할 수 있습니다.
seo-description: 점진적 JPEG 스캔 점진적 JPEG는 처음에 전체적으로 흐리거나 품질이 낮은 사진을 표시하는 방식으로 이미지를 표시합니다. 스캔이 계속 진행되면 이미지의 데이터가 더 완전히 다운로드되면 더 명확해집니다. 이 매개 변수를 사용하면 전체 이미지가 표시되도록 스캔 수(3, 4 또는 5)를 설정할 수 있습니다.
seo-title: pscan
solution: Experience Manager
title: pscan
topic: Scene7 Image Serving - Image Rendering API
uuid: c8e1d7a9-679c-437f-aa53-67aca3f40b30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pscan{#pscan}

점진적 JPEG 스캔 점진적 JPEG는 처음에 전체적으로 흐리거나 품질이 낮은 사진을 표시하는 방식으로 이미지를 표시합니다. 스캔이 계속 진행되면 이미지의 데이터가 더 완전히 다운로드되면 더 명확해집니다. 이 매개 변수를 사용하면 전체 이미지가 표시되도록 스캔 수(3, 4 또는 5)를 설정할 수 있습니다.

`pscan=auto|3|4|5`

각 스캔의 실제 속도는 사용자 시스템의 전송 속도와 데이터를 수신하고 압축 해제하는 컴퓨터의 전송 속도에 따라 달라집니다.

`Auto` 는 독립 JPEG 라이브러리에 의해 계산되고 색상 모델에 따라 결정되는 스캔 설정을 사용합니다. JPEG 파일을 `3`pjpeg로 저장할 때 Adobe `4`Photoshop에 있는 스캔 설정에 `5` 해당하는 값(점진적 JPEG)입니다.

이 `pscan` 설정되어 있지 않으면 기본값이 로 설정됩니다 `auto`.

## 속성 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다. 출력 형식이 점진적 JPEG가 아닌 경우 무시됩니다.

## 기본값 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 예 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 참조 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
