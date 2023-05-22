---
description: 레이어 0에 대해 레이어 크기 조정(size=) 및 위치 지정(pos=)을 수행하고 레이어= 명령으로 합성 순서(z-order)를 지정하는 것 외에도 레이어를 회전(rotate=)하고 대칭 이동(flip=)할 수 있습니다.
solution: Experience Manager
title: 레이어 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# 레이어 작업{#layer-operations}

레이어 0에 대해 레이어 크기 조정(size=) 및 위치 지정(pos=)을 수행하고 레이어= 명령으로 합성 순서(z-order)를 지정하는 것 외에도 레이어를 회전(rotate=)하고 대칭 이동(flip=)할 수 있습니다.

다음 `origin=` 및 `anchor=` 속성은 이미지 또는 텍스트가 템플릿에서 동적으로 변경될 때 레이어 간의 원하는 정렬을 유지하는 데 사용할 수 있습니다.

다음 `maskUse=` 이미지 레이어에서 별도의 마스크가 있는 이미지의 배경 영역에 액세스하는 명령을 사용할 수 있습니다.

`opac=` 를 사용하여 레이어 불투명도를 변경할 수 있습니다. `hide=` 레이어를 표시하거나 숨깁니다.
