---
description: 이미지에 대한 변환 보기
solution: Experience Manager
title: 이미지에 대한 변환 보기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
TQID: 'https://experienceleague.adobe.com/PPSeNhcaJ4Nx8ojXOt9vqJFp7F9NGo4LO3UxdLKzmwo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# 이미지에 대한 변환 보기{#view-transform-for-images}

`req=img` 요청에 대한 응답으로 클라이언트에 반환된 이미지는 `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix` 값과 복합 이미지의 크기를 고려하여 복합 이미지에서 파생됩니다.

`wid=` 및 `hei=`이(가) 지정되어 있고 `scl=`이(가) 지정되어 있지 않은 경우 합성 이미지는 `wid=` 및 `hei=`에 의해 정의된 보기 rect 내에 완전히 맞도록 크기가 조정됩니다. 뷰 rect의 종횡비가 합성 이미지의 종횡비와 다른 경우, 지정된 경우 배율 조정된 합성 이미지가 `align=` 값을 사용하여 뷰 rect 내에 정렬되거나 가운데에 정렬됩니다. 이미지 데이터에 포함되지 않은 모든 공간은 `bgc=` 또는 지정하지 않은 경우 `attribute::BkgColor`(으)로 채워집니다.

`scl=`이(가) 지정된 경우 합성 이미지는 해당 배율 계수로 조정됩니다. `wid=` 및/또는 `hei=`도 지정된 경우 필요에 따라 크기 조정된 이미지가 `wid=` 및/또는 `hei=`(으)로 잘리거나 추가 공간이 추가됩니다. `align=`은(는) 이미지를 자를 위치를 지정하거나 추가 공간을 추가하고 추가 공간은 `bgc=` 또는 `attribute::BkgColor`(으)로 채웁니다.

`wid=`, `hei=` 또는 `scl=`을(를) 지정하지 않고 합성 이미지의 너비 또는 높이가 `attribute::DefaultPix`을(를) 초과하면 합성 이미지가 `attribute::DefaultPix`을(를) 초과하지 않도록 크기가 조정됩니다. 그렇지 않으면 비율 조정 없이 합성 이미지가 사용됩니다.

더 이상 확대하지 않고 보기 이미지가 반환되도록 하려면 `scl=1`을(를) 지정하십시오.

`rgn=`을(를) 지정하면 응답 이미지가 그에 따라 잘려서 최종 응답 이미지 크기에 도달합니다. 이 크기는 `attribute::MaxPix`(정의된 경우)과 비교되며 응답 이미지가 두 차원에서 더 클 경우 오류가 생성됩니다.

`fmt=`에서 알파 없이 데이터를 지정하면 응답 이미지의 모든 투명 영역이 `bgc=` 또는 `attribute::BkgColor`(으)로 채워집니다.
