---
description: 이 섹션의 설정은 req=set 수정자가 획득한 미디어 세트 응답에 적용됩니다.
seo-description: 이 섹션의 설정은 req=set 수정자가 획득한 미디어 세트 응답에 적용됩니다.
seo-title: 미디어 집합 응답
solution: Experience Manager
title: 미디어 집합 응답
topic: Scene7 Image Serving - Image Rendering API
uuid: 9fa6a38a-cd1f-499b-a2b6-e1a9a6c69ed0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 미디어 집합 응답{#media-set-responses}

이 섹션의 설정은 req=set 수정자가 획득한 미디어 세트 응답에 적용됩니다.

## PS::fvctx.useCatalogRecordValidation - 캐싱 정책 {#section-9accb087d16548a988993bb30395a6f6}

이 속성은 캐시에서 검색되는 응답을 다시 생성해야 하는지 여부를 결정할 때 캐싱 정책을 제어합니다. 속성이 비활성화되면 [!DNL catalog.ini] 파일의 타임스탬프가 유효성 검사에 사용됩니다. 속성이 활성화되면 모든 참조된 레코드의 최신 `catalog::LastModified` 타임스탬프가 유효성 검사에 사용됩니다.

## PS::fvctx.nestingLimit - 중첩 제한 {#section-280210341f1647fea02590e7069934d2}

모든 `req=set` 응답의 최대 중첩 심도. 이 깊이를 초과하면 오류가 반환됩니다.

## PS::fvctx.brochureLimit - 브로셔 제한 {#section-fe36e47db49244cea7f07e9dd3639440}

모든 관련 메타데이터를 포함하는 응답의 최대 전자 카탈로그 브로셔 수입니다. `req=set` 이 제한이 초과되면 브로셔 항목과 연관된 모든 개인 맵과 사용자 데이터가 억제됩니다.
