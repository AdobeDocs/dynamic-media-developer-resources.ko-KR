---
description: 이러한 서버 설정을 사용하여 이미지 크기 제한을 설정합니다.
solution: Experience Manager
title: 이미지 크기 제한
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# 이미지 크기 제한{#image-size-limits}

이러한 서버 설정을 사용하여 이미지 크기 제한을 설정합니다.

## IS::MaxMessageSize - 응답 크기 제한 {#section-bd942385d4d144cd904003695d72c85e}

이미지 서버에서 [!DNL Platform Server]&#x200B;(으)로 보낼 수 있는 데이터 크기를 제한합니다. 효과적으로, 이미지 제공이 HTTP(MB)를 통해 클라이언트에 반환할 수 있는 인코딩/압축 응답 이미지의 크기를 제한합니다.

## IS::MaxRenderRgnPixels - 출력 이미지 크기 제한 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

이미지 서버에서 생성할 수 있는 이미지 크기를 제한합니다(파일에 저장된 이미지 제외). 백만 픽셀에서 0보다 큰 정수 값입니다. 렌더링 작업이 크기 제한을 초과할 경우 오류가 반환됩니다. 기본값은 16입니다.

## IS::MaxSavePixels - 파일에 저장하기 위한 크기 제한 {#section-d1547c4afa88467080ab08356f775e06}

`req=saveToFile` 명령을 사용하여 이미지 서버가 파일에 쓰는 이미지 크기를 제한합니다. 백만 픽셀에서 0보다 큰 정수 값입니다. 파일 저장 작업이 해당 제한을 초과하는 경우 오류가 반환됩니다. 기본값은 1억 픽셀입니다.

## IS::MaxNonDsfSize - PTIFF가 아닌 입력 이미지의 크기 제한 {#section-50de28a7158a436393cce5da0d1e4d46}

이미지 서버가 열 수 있는 PTIFF가 아닌 이미지의 최대 크기(Mpixel)입니다. 이 제한보다 큰 PTIFF가 아닌 이미지에 액세스하려고 하면 이미지 제공이 오류를 반환합니다.

>[!NOTE]
>
>이 값을 너무 높게 설정하면 이미지 서버에 메모리가 부족하여 충돌을 비롯한 오류가 발생할 수 있습니다.
