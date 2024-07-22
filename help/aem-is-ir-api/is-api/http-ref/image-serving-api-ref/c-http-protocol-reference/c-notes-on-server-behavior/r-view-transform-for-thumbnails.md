---
description: req=tmb 요청에 대한 응답으로 클라이언트에 반환되는 이미지는 다음 값 wid=, hei=, DefaultThumbPix 및 MaxPix를 고려하여 합성 이미지에서 파생됩니다.
solution: Experience Manager
title: 썸네일에 대한 변형 보기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# 썸네일에 대한 변형 보기{#view-transform-for-thumbnails}

req=tmb 요청에 대한 응답으로 클라이언트에 반환되는 이미지는 wid=, hei=, attribute::DefaultThumbPix 및 attribute::MaxPix 값을 고려하여 복합 이미지에서 파생됩니다.

1. **보기 rect 계산** - 보기 rect의 너비에 `wid=` 또는 너비 값 `attribute::DefaultThumbPix`을(를) 사용합니다. 높이에는 `hei=` 또는 `attribute::DefaultThumbPix`의 높이 값을 사용하십시오. 이 단계에서는 rect 보기를 완전히 지정해야 합니다. (레이어 0에 대해 `size=`이(가) 지정되지 않은 경우 뷰 rect는 레이어 0 rect와 동일합니다.)
1. **합성 크기 조정** - `catalog::ThumbType=Crop`인 경우 전체 보기 rect를 채우는 동안 가능한 가장 작은 이미지로 합성 크기가 조정됩니다. 추가 이미지 데이터는 잘립니다. `catalog::ThumbType= Fit`이면 전체 컴포지션을 뷰 rect에 맞추면서 가능한 가장 큰 이미지로 컴포지션의 크기가 조정됩니다. `catalog::ThumbType=Texture`인 경우 `catalog::ThumbRes`에 지정된 해상도를 유지하기 위해 합성 크기를 조정하지 않습니다.
1. **채우기 및 자르기** - 보기 rect가 `bgc=` 색상으로 채워집니다(지정되지 않은 경우 `attribute::ThumbBkgColor`). 크기가 조정된 조합이 `ThumbHorizAlign` 특성 및 `ThumbVertAlign` 특성을 사용하여 rect 보기에 맞게 정렬되었습니다. 그런 다음 배율 조정된 합계는 추가 배율 없이 채워진 뷰 사각형과 병합됩니다. 뷰 사각형을 넘어 확장되는 모든 합성 영역은 잘립니다.
