---
description: 레이어 0을 기준으로 레이어의 크기 조정(size=) 및 위치 지정(pos=) 레이어와 레이어= 명령을 사용하여 합성 순서(z 순서)를 지정하는 것 외에도 레이어를 회전(회전=)하고 뒤집기(뒤집기=)할 수 있습니다.
solution: Experience Manager
title: 레이어 작업
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# 레이어 작업{#layer-operations}

레이어 0을 기준으로 레이어의 크기 조정(size=) 및 위치 지정(pos=) 레이어와 레이어= 명령을 사용하여 합성 순서(z 순서)를 지정하는 것 외에도 레이어를 회전(회전=)하고 뒤집기(뒤집기=)할 수 있습니다.

템플릿에서 이미지 또는 텍스트가 동적으로 변경될 때 레이어 간에 원하는 정렬을 유지하는 데 `origin=` 및 `anchor=` 속성을 사용할 수 있습니다.

`maskUse=` 명령은 이미지 레이어에서 별도의 마스크가 있는 이미지의 배경 영역에 액세스할 수 있습니다.

`opac=` 레이어 불투명도를 변경하고 레이어 `hide=` 를 표시하거나 숨기는 데 사용할 수 있습니다.
