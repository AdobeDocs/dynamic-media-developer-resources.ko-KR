---
title: IR 3.x 호환성 모듈 설정 및 구성
description: IR 3.x 호환성 모듈을 설정하고 구성합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
TQID: 'https://experienceleague.adobe.com/ce7CdClFrrIFb7fhZRKQ7XBpsNm4BTgwVFHPXy3BXhw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 0%

---

# IR 3.x 호환성 모듈 설정 및 구성{#setup-and-configure-ir-x-compatibility-module}

1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>` 중지.
1. ImageServer 웹 앱 디렉토리로 변경합니다.
1. [!DNL ir] 디렉터리의 내용을 [!DNL `ROOT`] 디렉터리에 복사합니다.
1. 텍스트 편집기에서 [!DNL `ROOT/WEB-INF/web.xml`] 열기
1. `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->` 줄 검색
1. `<servlet>` 및 `<servlet-mapping>` 태그의 주석을 제거하십시오.
1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>` 다시 시작

**Linux® 예**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

그런 다음 좋아하는 편집기로 [!DNL `web.xml`]을(를) 편집하여 `<servlet>` 및 `<servlet-mapping>` 태그의 주석을 제거하십시오.

**Windows 예**

탐색기를 열고 `C:\Program Files\Scene7\ImageServing\webapps\ir`(으)로 이동합니다.

모든 파일과 폴더를 선택하고 `C:\Program Files\Scene7\ImageServing\webapps\ROOT` 내에 복사하십시오.

`c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml` 파일을 편집하여 `<servlet>` 및 `<servlet-mapping>` 태그의 주석을 제거하십시오.
