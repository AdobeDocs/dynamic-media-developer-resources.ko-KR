---
description: URL 또는 카탈로그 수정자 명령 시퀀스에서 레이어 정의 시퀀스는 layer= 명령으로 시작하여 다른 layer= 명령, effect= 명령 또는 URL의 끝으로 종료됩니다.
seo-description: URL 또는 카탈로그 수정자 명령 시퀀스에서 레이어 정의 시퀀스는 layer= 명령으로 시작하여 다른 layer= 명령, effect= 명령 또는 URL의 끝으로 종료됩니다.
seo-title: 레이어 지정
solution: Experience Manager
title: 레이어 지정
topic: Scene7 Image Serving - Image Rendering API
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# 레이어 지정{#specifying-layers}

URL 또는 catalog::Modifier 명령 시퀀스에서 레이어 정의 시퀀스는 layer= 명령으로 시작하여 다른 layer= 명령, effect= 명령 또는 URL의 끝으로 종료됩니다.

레이어 정의 시퀀스 내의 모든 명령은 레이어와 연결됩니다.

`layer=` 명령은 0보다 큰 정수여야 하는 레이어 번호를 지정합니다. 레이어 번호가 동일한 레이어 정의 시퀀스의 모든 명령이 동일한 레이어에 적용됩니다. 동일한 명령이 두 번 이상 발생하면 마지막 인스턴스가 우선합니다.
