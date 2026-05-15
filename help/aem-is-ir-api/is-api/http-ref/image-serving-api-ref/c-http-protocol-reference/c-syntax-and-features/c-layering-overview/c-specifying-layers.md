---
description: URL 또는 카탈로그 수정자 명령 시퀀스에서 레이어 정의 시퀀스는 layer= 명령으로 시작되고 다른 layer= 명령, effect= 명령 또는 URL의 끝으로 종료됩니다.
solution: Experience Manager
title: 레이어 지정
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
TQID: 'https://experienceleague.adobe.com/jNFpOYrBFWWc53JvzwENSjpM-SkIpenxxWPUgGX-p0Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 0%

---

# 레이어 지정{#specifying-layers}

URL 또는 catalog::Modifier 명령 시퀀스에서 레이어 정의 시퀀스는 layer= 명령으로 시작하여 다른 layer= 명령, effect= 명령 또는 URL의 끝으로 종료됩니다.

레이어 정의 시퀀스 내의 모든 명령은 레이어와 연관됩니다.

`layer=` 명령은 정수 0 이상이어야 하는 레이어 번호를 지정합니다. 레이어 번호가 같은 레이어 정의 시퀀스의 모든 명령이 동일한 레이어에 적용됩니다. 동일한 명령이 두 번 이상 발생하면 마지막 인스턴스가 우세합니다.
