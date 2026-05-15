---
title: 미디어 집합 응답
description: 이 섹션의 설정은 req=set 수정자가 얻은 미디어 세트 응답에 적용됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
TQID: 'https://experienceleague.adobe.com/FNUguOqf8f5FnIeGTzheZU-8zCXqwRMU3YGyvYDA0uM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 0%

---

# 미디어 집합 응답{#media-set-responses}

이 섹션의 설정은 `req=set` 한정자에서 얻은 미디어 집합 응답에 적용됩니다.

## PS::fvctx.useCatalogRecordValidation - 캐싱 정책 {#section-9accb087d16548a988993bb30395a6f6}

이 속성은 캐시에서 검색된 집합 응답을 다시 생성해야 하는지 여부를 결정할 때 캐싱 정책을 제어합니다. 속성을 사용하지 않도록 설정하면 [!DNL catalog.ini] 파일의 타임스탬프가 유효성 검사에 사용됩니다. 속성이 활성화된 경우 참조된 모든 레코드의 최신 `catalog::LastModified` 타임스탬프가 유효성 검사에 사용됩니다.

## PS::fvctx.nestingLimit - 중첩 제한 {#section-280210341f1647fea02590e7069934d2}

`req=set` 응답의 최대 중첩 깊이입니다. 이 깊이를 초과하면 오류가 반환됩니다.

## PS::fvctx.brochureLimit - 브로셔 제한 {#section-fe36e47db49244cea7f07e9dd3639440}

연결된 모든 메타데이터가 포함된 `req=set` 응답의 최대 전자 카탈로그 브로셔 수입니다. 이 제한을 초과하면 브로셔 항목과 연결된 모든 비공개 맵 및 사용자 데이터가 표시되지 않습니다.
