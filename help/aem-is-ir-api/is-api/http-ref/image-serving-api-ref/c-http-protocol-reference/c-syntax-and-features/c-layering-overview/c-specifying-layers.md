---
description: URL 또는 카탈로그 수정자 명령 시퀀스에서 레이어 정의 시퀀스는 layer= 명령으로 시작되며 다른 layer= 명령, effect= 명령 또는 URL의 끝으로 종료됩니다.
solution: Experience Manager
title: 레이어 지정
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# 레이어 지정{#specifying-layers}

URL 또는 catalog::Modifier 명령 시퀀스에서 레이어 정의 시퀀스는 layer= 명령으로 시작되고 다른 layer= 명령, effect= 명령 또는 URL의 끝으로 종료됩니다.

레이어 정의 시퀀스 내의 모든 명령은 레이어와 연관됩니다.

`layer=` 명령은 레이어 번호를 지정합니다. 이 값은 정수 0 이상이어야 합니다. 레이어 정의 시퀀스의 모든 명령은 동일한 레이어에 적용됩니다. 동일한 명령이 두 번 이상 발생하면 마지막 인스턴스가 우선합니다.
