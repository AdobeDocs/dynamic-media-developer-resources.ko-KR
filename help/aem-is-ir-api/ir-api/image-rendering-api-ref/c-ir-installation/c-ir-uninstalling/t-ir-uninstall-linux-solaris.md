---
description: 다음 지침에 따라 Linux 또는 Solaris 시스템에서 이미지 렌더링을 제거합니다.
solution: Experience Manager
title: Linux 및 Solaris에서 제거
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Linux 및 Solaris에서 제거{#uninstalling-on-linux-and-solaris}

다음 지침에 따라 Linux 또는 Solaris 시스템에서 이미지 렌더링을 제거합니다.

Linux 또는 Solaris 시스템에서 이미지 렌더링을 제거하는 방법에는 두 가지가 있습니다.

**방법 1**

1. 찾기 [!DNL uninstall.sh].

   ImageRendering이 설치된 디렉터리에 있습니다. 이 디렉토리를 제거한 경우 원래 설치 패키지를 압축하지 않고 압축을 해제하여 [!DNL uninstall.sh] 을 추출해야 합니다.
1. [!DNL uninstall.sh]을 실행하고 화면의 지침을 따릅니다.

>**방법 2**
>
>1. 다음 방법으로 ImageRendering을 중지합니다. ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. 시스템에서 ImageRendering을 제거합니다.

>
>   
ImageRendering을 제거하는 명령은 시스템에 따라 다릅니다.
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. 2단계에서 제거되지 않은 디렉토리 또는 파일을 모두 삭제합니다.

>


