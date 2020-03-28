---
description: 널
seo-description: 널
seo-title: 이미지의 변형 보기
solution: Experience Manager
title: 이미지의 변형 보기
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 이미지의 변형 보기{#view-transform-for-images}

요청에 대한 응답으로 클라이언트로 반환되는 이미지는 다음 값을 고려하여 복합 이미지에서 파생됩니다. `req=img` 합성 이미지의 `wid=``hei=`, `fit=``scl=`, `rgn=``attribute::DefaultPix`및 `attribute::MaxPix`크기

및 이 지정되어 있고 `wid=` 지정되지 않은 경우, 및 에 의해 정의된 뷰 rect 내에 완전히 맞도록 합성 이미지의 크기가 `hei=` 조절됩니다 `scl=` `wid=` `hei=`. 뷰 사각형의 종횡비가 합성 이미지의 종횡비와 다른 경우 크기가 조절된 합성 이미지가 `align=` 값을 사용하여 뷰 사각형 내에 정렬되거나, 그렇지 않으면 가운데에 정렬됩니다. 이미지 데이터로 포함되지 않은 모든 공간은 `bgc=` 또는 지정하지 않은 경우 으로 채워집니다 `attribute::BkgColor`.

이 `scl=` 값을 지정하면 합성 이미지의 배율이 해당 배율로 조절됩니다. 및/ `wid=` 또는 `hei=` 를 함께 지정하면 크기가 조정된 이미지가 `wid=` `hei=` 및/또는 추가 공간에 필요에 따라 추가됩니다. `align=` 이미지가 잘리거나 추가 공간이 추가되는 위치와 추가 공간이 `bgc=` 또는 `attribute::BkgColor`로 채워지는 위치를 지정합니다.

둘 다 `wid=`지정되지 `hei=` 않거나 `scl=` 지정되지 않은 경우 합성 이미지의 너비나 높이가 `attribute::DefaultPix`초과하면 합성 이미지의 크기가 `attribute::DefaultPix`초과하지 않도록 조절됩니다. 그렇지 않으면 비율 조정 없이 합성 이미지가 사용됩니다.

추가 크기 조정 없이 보기 이미지가 반환되도록 하려면 을 `scl=1`지정합니다.

이 `rgn=` 지정된 경우 회신 이미지가 잘려 최종 응답 이미지 크기에 도달합니다. 이 크기는 `attribute::MaxPix` (정의된 경우)와 비교되며, 응답 이미지가 두 차원 중 하나에서 클 경우 오류가 생성됩니다.

알파 없이 데이터를 `fmt=` 지정하면 응답 이미지의 모든 투명 영역이 `bgc=` 또는 `attribute::BkgColor`으로 채워집니다.
