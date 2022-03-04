---
description: req=tmb 요청에 대한 응답으로 클라이언트에 반환되는 이미지는 wd=, hei=, attribute DefaultThumbPix 및 MaxPix 속성을 고려하여 복합 이미지에서 파생됩니다.
solution: Experience Manager
title: 축소판 그림 변환 보기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# 축소판 그림 변환 보기{#view-transform-for-thumbnails}

req=tmb 요청에 대한 응답으로 클라이언트에 반환되는 이미지는 다음 값을 고려하여 복합 이미지에서 파생됩니다. wid=, hei=, attribute::DefaultThumbPix 및 attribute::MaxPix.

1. **뷰 레코드 계산** - 사용 `wid=` 또는 너비 값 `attribute::DefaultThumbPix` 를 클릭합니다. 사용 `hei=` 또는 높이 값 `attribute::DefaultThumbPix` 높이. 이 단계에서 뷰 레코드를 완전히 지정해야 합니다. (없는 경우 뷰 레코드는 레이어 0과 동일합니다 `size=`레이어 0에 대해 지정됩니다.)
1. **컴포지션의 비율 조정** - If `catalog::ThumbType=Crop`그런 다음 전체 보기 레코드를 채우는 동안 컴포지션이 가능한 가장 작은 이미지로 크기가 조절됩니다. 추가 이미지 데이터가 잘립니다. If `catalog::ThumbType= Fit`그런 다음 컴포지션이 가능한 가장 큰 이미지로 크기가 조절되고 전체 컴포지션이 보기 설명에 맞게 조정됩니다. If `catalog::ThumbType=Texture`에 지정된 해상도를 유지하기 위해 컴포지션의 크기가 전혀 조정되지 않습니다. `catalog::ThumbRes`.
1. **채우기 및 자르기** - 뷰 레코드 가 `bgc=` 색상(또는 지정하지 않은 경우, `attribute::ThumbBkgColor`). 스케일링된 컴포지션은 다음 속성을 사용하여 뷰 레코드와 정렬됩니다. `ThumbHorizAlign` 및 속성: `ThumbVertAlign`. 그런 다음 스케일링된 컴포지션이 다시 확장되지 않고 채워진 보기 레코드와 병합됩니다. 뷰 레코드 범위를 벗어나는 컴포지션의 모든 영역이 잘립니다.
