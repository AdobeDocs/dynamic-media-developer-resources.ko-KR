---
description: 이미지에 대한 변환 보기
solution: Experience Manager
title: 이미지에 대한 변환 보기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 이미지에 대한 변환 보기{#view-transform-for-images}

다음에 대한 응답으로 클라이언트에 반환된 이미지 `req=img` 요청은 다음 값을 고려하여 합성 이미지에서 파생됩니다. `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`및 합성 이미지의 크기입니다.

If `wid=` 및 `hei=` 및 `scl=` 은 아니지만, 합성 이미지는 다음에 의해 정의된 뷰 rect 내에 완전히 맞도록 크기가 조정됩니다. `wid=` 및 `hei=`. 뷰 rect의 종횡비가 합성 이미지의 종횡비와 상이한 경우, 스케일링된 합성 이미지는 다음을 사용하여 뷰 rect 내에서 정렬된다 `align=` 값(지정된 경우) 또는 가운데로 정렬됩니다. 이미지 데이터로 덮이지 않은 모든 공간은 `bgc=` 또는, 지정하지 않은 경우 `attribute::BkgColor`.

If `scl=` 를 지정하면 합성 이미지가 해당 배율 인자에 의해 배율이 조정됩니다. If `wid=` 및/또는 `hei=` 을 지정하면 배율 조정된 이미지가 잘려서 `wid=` 및/또는 `hei=` 또는 필요에 따라 추가 공간이 추가됩니다. `align=` 이미지를 자를 위치를 지정하거나 추가 공간을 추가하고 추가 공간을 채울 위치를 지정합니다. `bgc=` 또는 `attribute::BkgColor`.

둘 다 아닌 경우 `wid=`, `hei=` nor `scl=` 지정된 합성 이미지의 폭 또는 높이가 `attribute::DefaultPix`, 그런 다음 합성 이미지는 을 초과하지 않도록 크기가 조정됩니다. `attribute::DefaultPix`. 그렇지 않으면 비율 조정 없이 합성 이미지가 사용됩니다.

보기 이미지가 더 이상 확대되지 않고 반환되도록 하려면 을 지정합니다 `scl=1`.

If `rgn=` 을 지정하면 응답 이미지가 그에 따라 잘려서 최종 응답 이미지 크기에 도달합니다. 이 크기는 과(와) 비교됩니다. `attribute::MaxPix` (정의된 경우), 응답 이미지가 두 차원에서 더 큰 경우 오류가 생성됩니다.

If `fmt=` 알파 없이 데이터를 지정합니다. 응답 이미지의 모든 투명한 영역은 `bgc=` 또는 `attribute::BkgColor`.
