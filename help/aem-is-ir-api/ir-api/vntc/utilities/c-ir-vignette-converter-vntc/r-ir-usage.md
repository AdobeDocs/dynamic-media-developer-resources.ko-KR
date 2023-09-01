---
title: 사용
description: 이 항목에서는 vntc 사용 구문에 대해 설명합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---

# 사용{#usage}

이 항목에서는 vntc 사용 구문에 대해 설명합니다.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* 는 처리할 파일의 경로 및 이름입니다. 현재 작업 디렉토리에 상대적인 경로이거나 절대 경로일 수 있습니다. 유효한 비네팅, 캐비닛 스타일 또는 창 커버링 스타일 파일이어야 하며 다음 접미사 중 하나가 있어야 합니다.

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

필수.

*[!DNL destFile]* 는 출력 비네팅 파일의 경로 및 이름입니다. 지정하지 않으면 출력 파일이 로 지정된 폴더에 배치됩니다. `-destpath`. 이 시나리오에서는 입력 파일 이름과 크기 접미사를 로 구분하여 파일 이름이 자동으로 생성됩니다. `-separator`. 비네팅의 경우 크기 접미사는 단일 해상도 출력 비네팅의 픽셀 너비, 다중 해상도 출력 비네팅의 첫 번째 보기 너비 또는 피라미드 비네팅이 있는 경우 &#39;0&#39;입니다. 캐비닛 스타일 파일의 경우 출력 해상도가 파일 접미사로 사용됩니다. *[!DNL destFile]* 은(는) 다음의 경우 무시됩니다. `-info` 이(가) 지정되었습니다.
