---
title: 사용
description: 이 항목에서는 vntc 사용 구문에 대해 설명합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
TQID: 'https://experienceleague.adobe.com/uNh-n1OEJ5gxWBjLbBNutrNJ1Osae-PEOFBmaKNVf6c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 161
ht-degree: 1%

---

# 사용{#usage}

이 항목에서는 vntc 사용 구문에 대해 설명합니다.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]*&#x200B;은(는) 처리할 파일의 경로 및 이름입니다. 현재 작업 디렉토리에 상대적인 경로이거나 절대 경로일 수 있습니다. 유효한 비네팅, 캐비닛 스타일 또는 창 커버링 스타일 파일이어야 하며 다음 접미사 중 하나가 있어야 합니다.

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

필수.

*[!DNL destFile]*&#x200B;은(는) 출력 비네팅 파일의 경로 및 이름입니다. 지정하지 않으면 출력 파일이 `-destpath`(으)로 지정된 폴더에 배치됩니다. 이 시나리오에서는 입력 파일 이름과 크기 접미사를 `-separator`(으)로 지정된 문자열로 구분하여 파일 이름이 자동으로 생성됩니다. 비네팅의 경우 크기 접미사는 단일 해상도 출력 비네팅의 픽셀 너비, 다중 해상도 출력 비네팅의 첫 번째 보기 너비 또는 피라미드 비네팅이 있는 경우 &#39;0&#39;입니다. 캐비닛 스타일 파일의 경우 출력 해상도가 파일 접미사로 사용됩니다. `-info`을(를) 지정하면 *[!DNL destFile]*&#x200B;이(가) 무시됩니다.
