---
description: req=tmb 요청에 대한 응답으로 클라이언트에 반환되는 이미지는 wd=, hei=, attribute DefaultThumbPix 및 MaxPix 속성을 고려하여 복합 이미지에서 파생됩니다.
solution: Experience Manager
title: 축소판 그림 변환 보기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 축소판 그림 변환 보기{#view-transform-for-thumbnails}

req=tmb 요청에 대한 응답으로 클라이언트에 반환되는 이미지는 다음 값을 고려하여 복합 이미지에서 파생됩니다. wid=, hei=, attribute::DefaultThumbPix 및 attribute::MaxPix.

1. **뷰 레코드 계산**  - 뷰 레코드 너비 `wid=` 에  `attribute::DefaultThumbPix` 의 너비 또는 을 사용합니다. `hei=` 또는 `attribute::DefaultThumbPix` 높이 값을 높이로 사용합니다. 이 단계에서 뷰 레코드를 완전히 지정해야 합니다. ( 레이어 0에 대해 `size=`이 지정되지 않은 경우 뷰 레코드는 레이어 0과 동일합니다.)
1. **컴포지션의 비율 조정**  -  `catalog::ThumbType=Crop`이 조정되면 전체 보기 레코드를 채우는 동안 컴포지션이 가능한 가장 작은 이미지로 조정됩니다. 추가 이미지 데이터가 잘립니다. `catalog::ThumbType= Fit` 일 경우 컴포지션은 전체 컴포지션을 뷰 레코드에 연결하는 동안 가능한 가장 큰 이미지로 조정됩니다. `catalog::ThumbType=Texture`이면 컴포지션의 크기가 전혀 조절되지 않아 `catalog::ThumbRes`에 지정된 해상도를 유지할 수 있습니다.
1. **채우기 및 자르기**  - 보기 보고서 `bgc=` 에 색상이 채워집니다(또는 지정하지 않은 경우  `attribute::ThumbBkgColor`). 스케일링된 컴포지션은 다음 속성을 사용하여 뷰 레코드와 정렬됩니다. `ThumbHorizAlign` 및 특성: `ThumbVertAlign`. 그런 다음 스케일링된 컴포지션이 다시 확장되지 않고 채워진 보기 레코드와 병합됩니다. 뷰 레코드 범위를 벗어나는 컴포지션의 모든 영역이 잘립니다.
