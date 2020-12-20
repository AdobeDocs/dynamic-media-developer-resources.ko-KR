---
description: req=tmb 요청에 대한 응답으로 클라이언트에 반환된 이미지는 다음 값 wid=, hei=, attribute DefaultThumbPix 및 속성 MaxPix를 고려하여 합성 이미지에서 파생됩니다.
seo-description: req=tmb 요청에 대한 응답으로 클라이언트에 반환된 이미지는 다음 값 wid=, hei=, attribute DefaultThumbPix 및 속성 MaxPix를 고려하여 합성 이미지에서 파생됩니다.
seo-title: 축소판의 변형 보기
solution: Experience Manager
title: 축소판의 변형 보기
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 축소판 변환 보기{#view-transform-for-thumbnails}

req=tmb 요청에 대한 응답으로 클라이언트에 반환된 이미지는 다음 값을 고려하여 합성 이미지에서 파생됩니다.wid=, hei=, attribute::DefaultThumbPix 및 attribute::MaxPix.

1. **뷰 사각형 계산**  - 뷰 사각형 `wid=` 의 너비에  `attribute::DefaultThumbPix` 대한 사용 또는 너비 값을 계산합니다. 높이에 `hei=` 또는 `attribute::DefaultThumbPix`의 높이 값을 사용합니다. 이 단계에서 뷰 레코드를 완전히 지정해야 합니다. (레이어 0에 대해 `size=`이 지정되지 않은 경우 보기 레코드는 레이어 0 rect와 같습니다.)
1. **합성**  비율 조정 -  `catalog::ThumbType=Crop`전체 뷰 사각형을 채우는 동안 합성 이미지의 크기가 가능한 최소 이미지로 조절됩니다.추가 이미지 데이터가 잘립니다. `catalog::ThumbType= Fit`인 경우 전체 합성을 뷰 사각형에 맞추면서 가능한 가장 큰 이미지로 비율이 조정됩니다. `catalog::ThumbType=Texture`인 경우 합성은 `catalog::ThumbRes`에 지정된 해상도를 유지하기 위해 전혀 조정되지 않습니다.
1. **채우기 및 자르기**  - 뷰 사각형이  `bgc=` 색상으로 채워집니다(또는 지정하지 않은 경우 으로  `attribute::ThumbBkgColor`채워짐). 크기 조절된 합성은 다음과 같은 특성을 사용하여 뷰 맞춥니다.`ThumbHorizAlign` 및 속성:`ThumbVertAlign`. 크기가 조절된 합성은 추가 비율 조정 없이 채워진 보기 사각형과 병합됩니다. 뷰 사각형 이외의 합성 영역이 잘립니다.

