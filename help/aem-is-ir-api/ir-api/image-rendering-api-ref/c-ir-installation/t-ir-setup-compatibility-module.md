---
description: IR 3.x 호환성 모듈을 설정하고 구성해야 합니다.
solution: Experience Manager
title: IR 3.x 호환성 모듈 설정 및 구성
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---

# IR 3.x 호환성 모듈 설정 및 구성{#setup-and-configure-ir-x-compatibility-module}

IR 3.x 호환성 모듈을 설정하고 구성해야 합니다.

1. 중지 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. ImageServer 웹 앱 디렉토리로 변경합니다.
1. [!DNL ir] 디렉토리의 내용을 [!DNL ROOT] 디렉토리에 복사합니다.
1. 텍스트 편집기에서 [!DNL ROOT/WEB-INF/web.xml] 을 엽니다.
1. `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->` 줄을 검색합니다.
1. `<servlet>` 및 `<servlet-mapping>` 태그의 주석을 해제합니다.
1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`을(를) 다시 시작합니다.

**Linux 예**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

그런 다음 즐겨찾기 편집기를 사용하여 [!DNL web.xml]을 편집하여 `<servlet>` 및 `<servlet-mapping>` 태그의 주석을 해제합니다.

**Windows 예**

Explorer를 열고 `C:\Program Files\Scene7\ImageServing\webapps\ir`로 이동합니다.

모든 파일과 폴더를 선택하고 `C:\Program Files\Scene7\ImageServing\webapps\ROOT` 내부에 복사합니다.

그런 다음 `<servlet>` 및 `<servlet-mapping>` 태그의 주석을 해제하고 `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml` 파일을 편집합니다.
