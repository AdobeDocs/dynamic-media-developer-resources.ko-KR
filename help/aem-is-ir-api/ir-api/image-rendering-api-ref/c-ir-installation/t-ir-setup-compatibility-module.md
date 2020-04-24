---
description: IR 3.x 호환성 모듈을 설정하고 구성해야 합니다.
seo-description: IR 3.x 호환성 모듈을 설정하고 구성해야 합니다.
seo-title: IR 3.x 호환성 모듈 설정 및 구성
solution: Experience Manager
title: IR 3.x 호환성 모듈 설정 및 구성
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# IR 3.x 호환성 모듈 설정 및 구성{#setup-and-configure-ir-x-compatibility-module}

IR 3.x 호환성 모듈을 설정하고 구성해야 합니다.

1. 중지 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. ImageServer 웹 앱 디렉토리로 변경합니다.
1. 디렉토리의 컨텐츠를 [!DNL ir] [!DNL ROOT] 디렉토리로 복사합니다.
1. 텍스트 [!DNL ROOT/WEB-INF/web.xml] 편집기에서 엽니다.
1. 라인 검색 `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 및 `<servlet>` 태그의 주석을 `<servlet-mapping>` 해제합니다.
1. Restart `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux 예**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

자주 사용하는 편집기를 [!DNL web.xml]사용하여 편집하면 `<servlet>` 및 `<servlet-mapping>` 태그의 주석을 취소할 수 있습니다.

**Windows 예**

Explorer를 열고 로 `C:\Program Files\Scene7\ImageServing\webapps\ir`이동합니다.

모든 파일 및 폴더를 선택하고 안에 있는 파일을 복사합니다 `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

그런 다음 파일을 `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`편집하여 `<servlet>` 및 `<servlet-mapping>` 태그의 주석을 해제합니다.
