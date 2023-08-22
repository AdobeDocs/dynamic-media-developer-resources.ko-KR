---
title: pscan
description: 프로그레시브 JPEG 스캔. 점진적 JPEG은 초기에 흐릿하거나 낮은 품질의 사진을 전체적으로 표시하는 방식으로 이미지를 표시합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# pscan{#pscan}

프로그레시브 JPEG 스캔. 점진적 JPEG은 초기에 흐릿하거나 낮은 품질의 사진을 전체적으로 표시하는 방식으로 이미지를 표시합니다. 스캔 패스가 계속됨에 따라 이미지의 데이터가 더 완전히 다운로드될수록 더 명확해집니다. 이 매개 변수를 사용하면 전체 이미지를 표시하는 데 걸리는 스캔 횟수(3, 4 또는 5)를 설정할 수 있습니다.

`pscan=auto|3|4|5`

각각의 스캔의 실제 속도는 사용자의 시스템 및 데이터를 수신하고 압축을 푸는 컴퓨터의 전송 속도에 의존한다.

`Auto` 는 독립 JPEG 라이브러리에서 계산하고 색상 모델에 따라 달라지는 스캔 설정을 사용합니다. 값: `3`, `4`, `5` JPEG 파일을 pjpeg(프로그레시브 JPEG)로 저장할 때 Adobe Photoshop에 있는 스캔 설정에 해당합니다.

If `pscan` 가 설정되지 않은 경우 기본값이 로 설정됩니다. `auto`.

## 속성 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

요청 속성입니다. 현재 레이어 설정에 관계없이 적용됩니다. 출력 형식이 점진적 JPEG이 아닌 경우 무시됩니다.

## 기본값 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 예 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 참조 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
