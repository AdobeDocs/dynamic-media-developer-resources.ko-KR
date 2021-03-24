---
description: 이러한 서버 설정을 사용하여 이미지 크기 제한을 설정합니다.
solution: Experience Manager
title: 이미지 크기 제한
feature: Dynamic Media Classic,SDK/API
role: 개발자,관리자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# 이미지 크기 제한{#image-size-limits}

이러한 서버 설정을 사용하여 이미지 크기 제한을 설정합니다.

## IS::MaxMessageSize - 응답 크기 제한 {#section-bd942385d4d144cd904003695d72c85e}

이미지 서버가 플랫폼 서버로 보낼 수 있는 데이터의 크기를 제한합니다. 따라서 이미지 제공 기능이 HTTP(MB)를 통해 클라이언트로 돌아갈 수 있는 인코딩된/압축된 응답 이미지의 크기를 효과적으로 제한합니다.

## IS::MaxRenderRgnPixels - 출력 이미지 크기 제한 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

이미지 서버에서 생성할 수 있는 이미지의 크기를 제한합니다(파일에 저장된 이미지 제외). 수백만 픽셀의 정수 값이 0보다 큽니다. 렌더링 작업이 크기 제한을 초과할 경우 오류가 반환됩니다. 기본값은 16입니다.

## IS::MaxSavePixels - {#section-d1547c4afa88467080ab08356f775e06} 파일에 저장할 크기 제한

이미지 서버가 `req=saveToFile` 명령을 사용하여 파일에 기록할 이미지의 크기를 제한합니다. 수백만 픽셀의 정수 값이 0보다 큽니다. 파일 저장 작업이 해당 제한을 초과할 경우 오류가 반환됩니다. 기본값은 1억 픽셀입니다.

## IS::MaxNonDsfSize - 비PTIFF 입력 이미지의 크기 제한 {#section-50de28a7158a436393cce5da0d1e4d46}

이미지 서버가 열 수 있는 PTIFF가 아닌 이미지의 최대 크기(픽셀 단위)입니다. 이 제한보다 큰 PTIFF 이외의 이미지에 액세스하려고 하면 이미지 제공 시 오류가 반환됩니다.

>[!NOTE]
>
>이 값을 너무 높게 설정하면 이미지 서버에 메모리가 부족해지고 충돌을 포함한 오류가 발생할 수 있습니다.

