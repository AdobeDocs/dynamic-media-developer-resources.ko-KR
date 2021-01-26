---
description: 경로
solution: Experience Manager
title: 경로
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d1ed8a98-60eb-4bdb-884e-ea08c018d834
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 6%

---


# 경로{#path}

서버는 [소스 데이터 관리](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)에 설명된 경로 해결 규칙을 사용하여 데이터 파일을 찾습니다.

## 속성 {#section-72d9edc532ad43349afcb4df22e1c692}

텍스트 문자열. 이미지 및 SVG 레코드에 필요한 경우 템플릿 레코드에 대해 비어 있을 수 있습니다. 지정된 경우 올바른 상대 또는 절대 이미지 서버 파일 경로여야 합니다. 속성::DefaultExt는 파일 접미사가 없는 경우 추가됩니다.

## 지원되는 이미지 파일 형식 {#section-8d6443c883aa48aaa00316fe9661aaa8}

지원되는 이미지 파일 형식의 전체 목록은 IC(Image Converter) 유틸리티의 설명을 참조하십시오.

여러 해상도의 이미지 데이터가 필요한 응용 프로그램은 Dynamic Media PTIFF(Pyramid TIFF) 다중 해상도 형식을 사용할 때 가장 잘 수행됩니다. IC 유틸리티는 지원되는 모든 이미지 포맷에서 PTIFF 이미지를 만드는 데 사용됩니다.

## 기본값 {#section-82dad83ec3f84ae8bf2f850b4139f63e}

없음.

## 참조 {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[IC 유틸리티](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b),  [속성::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [속성::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0),  [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
