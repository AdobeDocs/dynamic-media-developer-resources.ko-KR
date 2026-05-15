---
description: 레이어 0에 대해 레이어 크기 조정(size=) 및 위치 지정(pos=)을 수행하고 레이어= 명령으로 합성 순서(z-order)를 지정하는 것 외에도 레이어를 회전(rotate=)하고 대칭 이동(flip=)할 수 있습니다.
solution: Experience Manager
title: 레이어 작업
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
TQID: 'https://experienceleague.adobe.com/uuGkOMzbkysv9BpR8zEK6dkuKgnseu3qwqLslA5W6zw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# 레이어 작업{#layer-operations}

레이어 0에 대해 레이어 크기 조정(size=) 및 위치 지정(pos=)을 수행하고 레이어= 명령으로 합성 순서(z-order)를 지정하는 것 외에도 레이어를 회전(rotate=)하고 대칭 이동(flip=)할 수 있습니다.

`origin=` 및 `anchor=` 특성은 이미지 또는 텍스트가 템플릿에서 동적으로 변경될 때 레이어 간의 원하는 정렬을 유지하는 데 사용할 수 있습니다.

`maskUse=` 명령은 이미지 레이어에서 별도의 마스크가 있는 이미지의 배경 영역에 액세스하는 데 사용할 수 있습니다.

`opac=`을(를) 사용하여 레이어 불투명도를 변경하고 `hide=`을(를) 사용하여 레이어를 표시하거나 숨길 수 있습니다.
