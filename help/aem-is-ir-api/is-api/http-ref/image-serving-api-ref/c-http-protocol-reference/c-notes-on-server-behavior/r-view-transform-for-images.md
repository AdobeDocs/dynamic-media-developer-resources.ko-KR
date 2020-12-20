---
description: 널
seo-description: 널
seo-title: 이미지에 대한 변형 보기
solution: Experience Manager
title: 이미지에 대한 변형 보기
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# 이미지에 대한 변형 보기{#view-transform-for-images}

`req=img` 요청에 응답하여 클라이언트에 반환된 이미지는 다음 값을 고려하여 합성 이미지에서 파생됩니다.`wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` 및 합성 이미지의 크기입니다.

`wid=` 및 `hei=`이 지정되어 있고 `scl=`가 지정되지 않은 경우 `wid=` 및 `hei=`에서 정의한 뷰 레코드 수에 완전히 맞도록 합성 이미지의 크기가 조절됩니다. 뷰 사각형의 종횡비가 합성 이미지의 종횡비와 다른 경우, 크기가 조절된 합성 이미지가 `align=` 값을 사용하여 뷰 사각형 내에 정렬되거나, 그렇지 않으면 가운데에 정렬됩니다. 이미지 데이터로 덮이지 않은 모든 공간은 `bgc=` 또는 지정되지 않은 경우 `attribute::BkgColor`로 채워집니다.

`scl=`이(가) 지정된 경우 합성 이미지의 배율이 해당 배율로 조정됩니다. `wid=` 및/또는 `hei=`도 지정된 경우 크기가 조정된 이미지가 `wid=` 및/또는 `hei=`에 잘리거나 필요에 따라 추가 공간이 추가됩니다. `align=` 이미지를 잘리거나 추가 공간을 추가할 위치와 추가 공간을  `bgc=` 또는 `attribute::BkgColor`로 채웁니다.

`wid=`, `hei=` 또는 `scl=`를 지정하지 않고 합성 이미지의 폭이나 높이가 `attribute::DefaultPix`을 초과하는 경우 합성 이미지의 크기가 `attribute::DefaultPix`를 초과하지 않도록 조절됩니다. 그렇지 않으면 비율 조정 없이 합성 이미지가 사용됩니다.

추가 크기 조정 없이 보기 이미지가 반환되도록 하려면 `scl=1`을 지정합니다.

`rgn=`이(가) 지정된 경우 응답 이미지가 그에 따라 잘려서 최종 응답 이미지 크기에 도달합니다. 이 크기는 `attribute::MaxPix`(정의된 경우)과 비교되며, 응답 이미지가 두 차원 중 하나에서 더 큰 경우 오류가 생성됩니다.

`fmt=`이 알파 없이 데이터를 지정하는 경우 응답 이미지의 모든 투명한 영역은 `bgc=` 또는 `attribute::BkgColor`로 채워집니다.
