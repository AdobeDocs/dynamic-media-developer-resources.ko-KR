---
description: 이 항목에서는 vntc 사용 구문에 대해 설명합니다.
solution: Experience Manager
title: 사용
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# 사용{#usage}

이 항목에서는 vntc 사용 구문에 대해 설명합니다.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* 는 처리할 파일의 경로와 이름입니다. 현재 작업 디렉토리나 절대 경로를 기준으로 한 경로일 수 있습니다. 유효한 비네팅, 캐비닛 스타일 또는 윈도우 커버 스타일 파일이어야 하며 다음 접미어 중 하나가 있어야 합니다.[!DNL .vnt], [!DNL .vnc] 또는 [!DNL .vnw]. 필수.

*[!DNL destFile]* 는 출력 비네팅 파일의 경로와 이름입니다. 지정하지 않으면 출력 파일이 `-destpath`으로 지정된 폴더에 배치됩니다. 이 시나리오에서는 파일 이름이 입력 파일 이름과 크기 접미어에서 자동으로 생성되며 이 이름은 `-separator`으로 지정된 문자열로 구분됩니다. 비네팅의 경우 크기 접미어는 단일 해상도 출력 비네팅의 픽셀 너비, 다중 해상도 출력 비네팅의 첫 번째 보기 너비 또는 피라미드 비네팅의 경우 &#39;0&#39;입니다. 캐비닛 스타일 파일의 경우 출력 해상도는 파일 접미어로 사용됩니다. *[!DNL destFile]* 이 지정되어 있으면  `-info` 무시됩니다.
