---
title: IR 3.x 호환성 모듈 설정 및 구성
description: IR 3.x 호환성 모듈을 설정하고 구성합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# IR 3.x 호환성 모듈 설정 및 구성{#setup-and-configure-ir-x-compatibility-module}

1. 중지 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. ImageServer 웹 앱 디렉토리로 변경합니다.
1. 의 내용을 복사합니다. [!DNL ir] 디렉토리 입력 [!DNL `ROOT`] 디렉토리.
1. 열기 [!DNL `ROOT/WEB-INF/web.xml`] 텍스트 편집기에서.
1. 라인 검색 `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. 주석 제거 `<servlet>` 및 `<servlet-mapping>` 태그 사이에 코드를 삽입하지 마십시오.
1. 다시 시작 `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux® 예**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

편집 [!DNL `web.xml`] 즐겨찾는 편집기를 사용하여 주석 달기 취소 `<servlet>` 및 `<servlet-mapping>` 태그 사이에 코드를 삽입하지 마십시오.

**Windows 예**

Explorer를 열고 다음으로 이동 `C:\Program Files\Scene7\ImageServing\webapps\ir`.

모든 파일과 폴더를 선택하고 내부에 복사합니다. `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

그런 다음 파일을 편집합니다 `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, 주석 달기 해제 `<servlet>` 및 `<servlet-mapping>` 태그 사이에 코드를 삽입하지 마십시오.
