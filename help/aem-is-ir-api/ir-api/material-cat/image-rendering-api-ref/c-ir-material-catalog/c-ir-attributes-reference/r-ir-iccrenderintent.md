---
title: IccRenderIntent
description: 색상 변환 렌더링 의도. 렌더링 의도가 'icc='로 지정되지 않은 경우 색상 변환에 대한 기본 렌더링 의도를 제공합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
TQID: 'https://experienceleague.adobe.com/5BehWh36v-kv7Z8kSj-WwoqBgyk4TC8srAhxKs89mnE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 2%

---

# IccRenderIntent{#iccrenderintent}

색상 변환 렌더링 의도. 렌더링 의도가 `icc=`에 지정되어 있지 않은 경우 색상 변환에 대한 기본 렌더링 의도를 제공합니다.

## 속성 {#section-0a38c60e1525426185616c42824aee2c}

열거형. 지각 0, 상대 색도계 1, 채도 2, 절대 색도계 3으로 설정합니다. 색상 프로파일에 정의된 기본 렌더링 의도를 사용할 수 있도록 비워 두거나 다른 값으로 설정합니다.

## 기본값 {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

정의되지 않은 경우 `default::IccRenderIntent`에서 상속됩니다. 비어 있으면 &#39;상대 색도계&#39;가 적용됩니다.

## 참조 {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)

