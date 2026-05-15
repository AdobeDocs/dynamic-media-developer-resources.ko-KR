---
description: 이미지 앵커. 이 이미지를 템플릿이나 합성 이미지의 레이어로 사용할 때의 원점입니다.
solution: Experience Manager
title: 앵커
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
TQID: 'https://experienceleague.adobe.com/OKTbXTF3uzVcQeLQIGIJhCukQFzdW5gZMzatSdWP7yY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 4%

---

# 앵커{#anchor}

이미지 앵커. 이 이미지를 템플릿이나 합성 이미지의 레이어로 사용할 때의 원점입니다.

또한 회전의 기본 중심점을 정의합니다.

## 속성 {#section-95740f14160744e7bc763094b8be40d8}

쉼표로 구분된 2개의 정수. 전체 해상도 이미지의 위쪽, 왼쪽 모서리를 기준으로 한 픽셀 오프셋입니다.

`anchor=`에 의해 재정의됩니다. `origin=`(으)로 재정의할 수 있습니다.

## 기본값 {#section-ca3a4cc837d643519eff15951f2b47a1}

이 필드가 없거나 비어 있는 경우, 그리고 올바른 이미지 레코드인 경우(즉, `catalog::Path`이(가) 올바른 경우) 이미지의 중심점이 사용됩니다.

## 참조 {#section-f605d29c3f5d48ad8e2a374f11886f19}

[앵커=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [원본=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
