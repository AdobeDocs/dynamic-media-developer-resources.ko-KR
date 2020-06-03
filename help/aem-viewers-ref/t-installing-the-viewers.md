---
description: Dynamic Media Viewers API 설치 지침
seo-description: Dynamic Media Viewers API 설치 지침
seo-title: 동일한 서버에 여러 뷰어 설치
solution: Experience Manager
title: 동일한 서버에 여러 뷰어 설치
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: a0983053795cc119eb57386c005e1f8a7c2fa3e4
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# 동일한 서버에 여러 뷰어 설치{#installing-multiple-viewers-on-the-same-server}

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Dynamic Media 뷰어 API 설치 지침

Image Serving 뷰어를 설치하기 전에 Image Serving을 설치하고 테스트합니다.

IS 뷰어 파일을 하드 드라이브에 복사한 다음 해당 `s7viewers.war` 파일을 `../ImageServing/webapps` 디렉토리에 배포합니다. 이미지 서버를 배포, 시작, 중지 및 관리하는 방법에 대한 지침은 이미지 제공 설명서를 참조하십시오.

>[!NOTE]
>
>Image Serving 뷰어에는 업그레이드 설치가 없습니다. 설치를 계속하기 전에 기존 Dynamic Media 뷰어 디렉토리를 백업하는 것이 좋습니다.

**동일한 서버에 뷰어를 설치하려면**

1. 뷰어 .war의 이름을 원하는 컨텍스트로 변경하고 파일을 원하는 위치에 배포합니다.
1. 매개 변수 `this.isViewerRoot` 를 설정합니다 `config.js`.
1. 새로 만든 뷰어 폴더의 루트에 `config.js` 있는 파일을 엽니다.
1. 매개 변수 `this.isViewerRoot = "/s7viewers"` 를 `s7viewers.war` 파일 컨텍스트에 설정합니다. (예: `"/s7viewers-4.0"`) 파일을 저장하고 닫습니다.
1. 파일을 저장하고 닫습니다.
