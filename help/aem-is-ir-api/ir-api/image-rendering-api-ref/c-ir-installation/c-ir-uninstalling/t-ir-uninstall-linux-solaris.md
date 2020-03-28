---
description: 다음 지침에 따라 Linux 또는 Solaris 시스템에서 이미지 렌더링을 제거합니다.
seo-description: 다음 지침에 따라 Linux 또는 Solaris 시스템에서 이미지 렌더링을 제거합니다.
seo-title: Linux 및 Solaris에서 제거
solution: Experience Manager
title: Linux 및 Solaris에서 제거
topic: Scene7 Image Serving - Image Rendering API
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Linux 및 Solaris에서 제거{#uninstalling-on-linux-and-solaris}

다음 지침에 따라 Linux 또는 Solaris 시스템에서 이미지 렌더링을 제거합니다.

Linux 또는 Solaris 시스템에서 이미지 렌더링을 제거하는 방법에는 두 가지가 있습니다.

**방법 1**

1. 찾기 [!DNL uninstall.sh].

   ImageRendering이 설치된 디렉토리에 있습니다. 이 디렉토리를 제거한 경우 추출하려면 원래 설치 패키지의 압축을 해제하고 압축을 해제해야 [!DNL uninstall.sh]합니다.
1. 화면의 지침에 [!DNL uninstall.sh] 따라 실행하십시오.
>**방법 2**
>
>1. ImageRendering 중지: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. 시스템에서 ImageRendering을 제거합니다.
>
>   
ImageRendering 제거 명령은 시스템에 따라 다릅니다.
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. 2단계에서 제거되지 않은 디렉토리 또는 파일을 삭제합니다.
>



