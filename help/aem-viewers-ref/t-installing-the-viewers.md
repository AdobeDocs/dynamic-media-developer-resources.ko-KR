---
title: 동일한 서버에 여러 Dynamic Media 뷰어 설치
description: Dynamic Media 뷰어 API 설치 지침
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
translation-type: tm+mt
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---

# 동일한 서버에 여러 뷰어 설치{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Dynamic Media 뷰어 API 설치 지침

이미지 제공 뷰어를 설치하기 전에 이미지 제공 서비스를 설치하고 테스트합니다.

IS 뷰어 파일을 하드 드라이브에 복사한 다음 `s7viewers.war` 파일을 `../ImageServing/webapps` 디렉토리로 배포합니다. 이미지 서버를 배포, 시작, 중지 및 관리하는 방법에 대한 지침은 이미지 제공 설명서를 참조하십시오.

>[!NOTE]
>
>이미지 제공 뷰어에는 업그레이드 설치가 없습니다. 설치를 계속하기 전에 기존 Dynamic Media 뷰어(s7viewers) 디렉토리를 백업하는 것이 좋습니다.

**동일한 서버에 여러 뷰어를 설치하려면:**

1. 뷰어 .war의 이름을 원하는 컨텍스트로 변경하고 파일을 원하는 위치에 배포합니다.
1. `config.js`에서 `this.isViewerRoot` 매개 변수를 설정합니다.
1. 새로 만든 뷰어 폴더의 루트에서 `config.js`을(를) 엽니다.
1. 매개 변수 `this.isViewerRoot = "/s7viewers"`을 `s7viewers.war` 파일의 컨텍스트에 설정합니다. (예: `"/s7viewers-4.0"`)
1. 파일을 저장하고 닫습니다.
