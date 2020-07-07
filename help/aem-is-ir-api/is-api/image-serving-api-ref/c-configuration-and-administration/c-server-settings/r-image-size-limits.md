---
description: 이러한 서버 설정을 사용하여 이미지 크기 제한을 설정합니다.
seo-description: 이러한 서버 설정을 사용하여 이미지 크기 제한을 설정합니다.
seo-title: 이미지 크기 제한
solution: Experience Manager
title: 이미지 크기 제한
topic: Scene7 Image Serving - Image Rendering API
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# 이미지 크기 제한{#image-size-limits}

이러한 서버 설정을 사용하여 이미지 크기 제한을 설정합니다.

## IS::MaxMessageSize - 응답 크기 제한 {#section-bd942385d4d144cd904003695d72c85e}

이미지 서버가 Platform 서버로 전송할 수 있는 데이터의 크기를 제한합니다. 따라서 Image Serving이 HTTP(Mbytes)를 통해 클라이언트로 돌아갈 수 있는 인코딩된/압축 응답 이미지의 크기가 효과적으로 제한됩니다.

## IS::MaxRenderRgnPixels - 출력 이미지 크기 제한 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

이미지 서버에서 생성할 수 있는 이미지 크기(파일에 저장된 이미지 제외)를 제한합니다. 0보다 큰 정수 값(수백만 픽셀) 렌더링 작업이 크기 제한을 초과할 경우 오류가 반환됩니다. 기본값은 16입니다.

## IS::MaxSavePixels - 파일에 저장할 수 있는 크기 제한 {#section-d1547c4afa88467080ab08356f775e06}

이미지 서버가 명령으로 파일에 기록할 이미지의 크기를 `req=saveToFile` 제한합니다. 0보다 큰 정수 값(수백만 픽셀) 파일 저장 작업이 해당 제한을 초과할 경우 오류가 반환됩니다. 기본값은 1억픽셀입니다.

## IS::MaxNonDsfSize - 비PTIFF 입력 이미지의 크기 제한 {#section-50de28a7158a436393cce5da0d1e4d46}

이미지 서버가 열 수 있는 PTIFF가 아닌 이미지의 최대 크기(픽셀 단위)입니다. 이 제한보다 큰 비PTIFF 이미지에 액세스하려고 하면 이미지 제공 시 오류가 반환됩니다.

>[!NOTE]
>
>이 값을 너무 높게 설정하면 이미지 서버에 메모리가 부족해지고 충돌을 포함한 오류가 발생할 수 있습니다.

