---
description: Vignette Converter(vntc)는 이미지 렌더링 을 사용하여 배포할 이미지 작성으로 만든 컨텐츠를 준비하는 데 사용되는 명령줄 유틸리티입니다.
solution: Experience Manager
title: 비네팅 변환기
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# 비네팅 변환기{#vignette-converter}

Vignette Converter(vntc)는 이미지 렌더링 을 사용하여 배포할 이미지 작성으로 만든 컨텐츠를 준비하는 데 사용되는 명령줄 유틸리티입니다.

[!DNL vntc] 는 [!DNL \ImageServing\bin]에  *[!DNL install_root]*&#x200B;있습니다. 여기에는 다음 기능이 있습니다.

* 기본 비네팅을 단일 해상도, 다중 해상도 또는 피라미드형 프로덕션 비네트로 변환합니다( [Vignette Scaling](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585) 참조).
* 스타일 파일을 포함하는 프로덕션 캐비닛 및 창을 생성합니다( `-resolution` 및 `-jpegquality` 참조).

* 이전 버전의 이미지 렌더링에 사용할 다양한 파일 버전의 비네팅, 캐비닛 및 창 커버 스타일 파일을 생성할 수 있습니다.
* 전체 해상도 또는 축소판에서 보기 이미지를 추출합니다( `-thumbwidth` 및 `-image` 참조).
* 소스 파일(`-info` 참조)에서 관련 속성을 추출하여 `stdout` 또는 선택적 로그 파일로 보냅니다( `-log` 참조).

[!DNL vntc]은(는) 선택 사항이지만 최상의 서버 성능을 위해서는 적극 사용하는 것이 좋습니다. [!DNL vntc] 또한 광범위한 오류 검사를 구현하고, 자주 사용하는 경우 충돌을 포함한 심각한 서버 문제를 방지할 수 있습니다.

프로덕션 비네팅을 생성할 때 출력 비네트의 픽셀 너비(또는 피라미드 또는 다중 해상도 비네팅의 경우 0)가 생성된 출력 비네팅 파일의 이름에 추가됩니다. 캐비닛 스타일 파일을 처리할 때 출력 해상도가 출력 파일 이름에 추가됩니다. 선택 사항인 축소판, 이미지 및 로그 파일과 프로덕션 비네팅 또는 캐비닛 스타일 파일을 포함한 모든 출력 파일은 `-destPath`이 지정된 경우가 아니면 *[!DNL sourceFile]*&#x200B;이 있는 동일한 디렉토리에 배치됩니다.

[!DNL vntc] 기본적으로 최대 3GB의 메모리로 제한됩니다. Vntc가 이 제한에 도달하면 처리가 중지되고 오류가 발생합니다. 이 제한은 `-maxmem` 을 사용하여 변경할 수 있습니다.

>[!NOTE]
>
>이미지 작성의 비네팅 업데이트 도구를 사용하여 이미지 렌더링 사용을 위한 비네팅을 준비할 수도 있습니다. 마찬가지로 컨텐츠 작성 도구에서는 이미지 렌더링에 사용할 캐비닛 스타일 파일을 생성할 수 있습니다. 처리를 자동화하려면 [!DNL vntc] 을 사용하십시오. 이미지 작성 의 도구에는 그래픽 사용자 인터페이스가 포함되어 있으므로 일반적으로 대화식으로 쉽게 사용할 수 있습니다.

## 참조 {#section-3c756bf17b634543904fdd928adeafb2}

이미지 작성 설명서
