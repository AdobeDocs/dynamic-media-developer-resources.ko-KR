---
title: 중첩된 요청에서 변수 처리
description: $var$ 참조는 쿼리와 경로를 구분하는 '?' 왼쪽을 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내 아무 곳에나 발생할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
TQID: 'https://experienceleague.adobe.com/m7BlSGU8gSozgp8fvNcWuMz5uvpUrfMi4fV5yCYH5bs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# 중첩된 요청에서 변수 처리{#variable-processing-in-nested-requests}

$var$ 참조는 쿼리와 경로를 구분하는 &#39;?&#39; 왼쪽을 포함하여 중첩된 이미지 제공 또는 이미지 렌더링 요청의 중괄호 내 아무 곳에나 발생할 수 있습니다.

서버는 중첩 요청을 추가로 구문 분석하고 처리하기 전에 이러한 참조를 값(URL 또는 기본 이미지 카탈로그의 `catalog::Modifier`에서)으로 대체합니다.

또한 URL 및 `catalog::Modifier`의 모든 `$ *[!DNL var]*=` 정의가 모든 중첩 이미지 제공 및 이미지 렌더링 요청으로 전달됩니다. 이렇게 하면 중첩 수준에 관계없이 모든 템플릿에서 모든 변수 정의를 사용할 수 있습니다.

중첩 수준에 관계없이, 중첩된 이미지 렌더링 또는 이미지 제공 요청의 모든 위치에서 대체할 변수 값에는 단일 패스 HTTP 인코딩만 적용해야 합니다.

