---
title: 제한 사항
description: 일부 제한 사항은 중첩 및 포함에 적용됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
TQID: 'https://experienceleague.adobe.com/rwy6ZnKA0pc-z-dqhsI0gD-FSqpqZr1bcIgJqtsjfIs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# 제한 사항{#restrictions}

일부 제한 사항은 중첩 및 포함에 적용됩니다.

서버 성능이 좋으려면 중첩 요청에서 반환된 이미지의 해상도가 재료가 적용되는 객체의 텍스처 해상도와 합리적으로 일치해야 합니다.

외부 이미지가 로컬에서 캐시됩니다. 이러한 이미지에 대한 모든 변경 사항은 로컬 캐시 항목이 오래된 경우에만 감지됩니다(만료 HTTP 헤더 기반).

