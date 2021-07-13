---
description: 기본 이미지 모드. 요청에 지정된 이미지를 찾을 수 없을 때 기본 이미지가 적용되는 방식을 선택합니다.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# DefaultImageMode{#defaultimagemode}

기본 이미지 모드. 요청에 지정된 이미지를 찾을 수 없을 때 기본 이미지가 적용되는 방식을 선택합니다.

## 속성 {#section-7fa8acb63540490d9f5186231b5e77c3}

열거형. 누락된 이미지가 여러 레이어 중 하나에 불과하더라도 전체 합성 이미지를 바꾸기 위한 &#39;0&#39; 누락된 각 레이어 소스 이미지를 기본 이미지로 바꾸고 컴포지션을 평소대로 반환하려면 &#39;1&#39;.

## 제한 사항 {#section-04cb0d50e8914564a8d226d0d4663c8b}

이미지 제공은 중첩된 이미지 렌더링, FXG 또는 `req=set` 요청이 실패하면 다시 `DefaultImageMode=0`로 되돌아갑니다.

## 기본값 {#section-9e318524a2a5496386901286748c7ee7}

정의되지 않았거나 비어 있는 경우 `default::DefaultImage`에서 상속됩니다.

## 참조 {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
