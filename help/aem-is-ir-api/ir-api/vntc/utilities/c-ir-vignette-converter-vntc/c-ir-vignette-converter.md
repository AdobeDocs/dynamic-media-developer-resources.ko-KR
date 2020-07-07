---
description: Vignette Converter(vntc)는 이미지 렌더링을 사용하여 배포하기 위해 이미지 작성으로 만든 컨텐츠를 준비하는 데 사용되는 명령줄 유틸리티입니다.
seo-description: Vignette Converter(vntc)는 이미지 렌더링을 사용하여 배포하기 위해 이미지 작성으로 만든 컨텐츠를 준비하는 데 사용되는 명령줄 유틸리티입니다.
seo-title: 비네팅 변환기
solution: Experience Manager
title: 비네팅 변환기
topic: Scene7 Image Serving - Image Rendering API
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# 비네팅 변환기{#vignette-converter}

Vignette Converter(vntc)는 이미지 렌더링을 사용하여 배포하기 위해 이미지 작성으로 만든 컨텐츠를 준비하는 데 사용되는 명령줄 유틸리티입니다.

[!DNL vntc] 은 [!DNL \ImageServing\bin]에 *[!DNL install_root]*&#x200B;있습니다. 다음과 같은 기능이 있습니다.

* 기본 비네팅을 단일 해상도, 다중 해상도 또는 피라미드형 제작 비네팅으로 변환합니다(비네팅 크기 조절 [참조](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* 프로덕션 캐비넷과 윈도우를 덮는 스타일 파일을 만듭니다( `-resolution` 및 참조 `-jpegquality`).

* 이전 버전의 이미지 렌더링에서 사용할 수 있도록 다양한 파일 버전의 비네팅, 캐비닛 및 창 커버 스타일 파일을 만들 수 있습니다.
* 전체 해상도 또는 축소판에서 보기 이미지를 추출합니다( `-thumbwidth` 및 `-image`참조).
* 소스 파일(참조)에서 관련 속성을 추출하여 `-info`또는 선택적 로그 파일(참조)로 전송합니다 `stdout` `-log`.

은(는) 선택 사항이지만, 최상의 서버 성능 [!DNL vntc] 을 위해 권장됩니다. [!DNL vntc] 또한 광범위한 오류 검사를 구현하며, 오류 발생 등 심각한 서버 문제를 사전에 방지할 수 있습니다.

프로덕션 비네팅을 생성할 때 출력 비네팅의 픽셀 너비(피라미드 또는 다중 해상도 비네팅의 경우 0)가 생성된 출력 비네팅 파일의 이름에 추가됩니다. 캐비닛 스타일 파일을 처리할 때 출력 해상도가 출력 파일 이름에 추가됩니다. 선택적인 축소판, 이미지 및 로그 파일과 프로덕션 비네팅 또는 캐비닛 스타일 파일을 포함한 모든 출력 파일은 지정된 경우가 아니면 위치한 동일한 디렉토리 *[!DNL sourceFile]* 에 배치됩니다 `-destPath` .

[!DNL vntc] 기본적으로 최대 3GB의 메모리로 제한됩니다. Vntc가 이 제한에 도달하면 처리가 중지되고 오류가 발생합니다. 이 제한은 를 사용하여 변경할 수 있습니다 `-maxmem`.

>[!NOTE]
>
>이미지 작성의 비네팅 업데이트 도구를 사용하여 이미지 렌더링 사용을 위한 비네팅을 준비할 수도 있습니다. 마찬가지로 컨텐츠 작성 툴에서도 이미지 렌더링에 사용할 캐비닛 스타일 파일을 생성할 수 있습니다. 처리를 자동화하려면 [!DNL vntc] 사용합니다. 이미지 작성의 도구에는 그래픽 사용자 인터페이스가 포함되어 있으므로 일반적으로 상호 작용 방식으로 사용하기 쉽습니다.

## 참조 {#section-3c756bf17b634543904fdd928adeafb2}

이미지 작성 설명서
