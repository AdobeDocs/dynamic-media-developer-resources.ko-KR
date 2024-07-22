---
title: Linux® 및 Solaris™에서 제거
description: Linux® 또는 Solaris™ 시스템에서 이미지 렌더링을 제거하려면 다음 지침을 따르십시오.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# Linux® 및 Solaris™에서 제거{#uninstalling-on-linux-and-solaris}

Linux® 또는 Solaris™ 시스템에서 이미지 렌더링을 제거하려면 다음 지침을 따르십시오. 사용할 수 있는 방법에는 두 가지가 있습니다. 다음 중 하나를 수행하십시오.

## 방법 1

1. [!DNL uninstall.sh] 찾기.

   ImageRendering이 설치된 디렉토리에 있습니다. 이 디렉터리를 제거한 경우 [!DNL uninstall.sh]을(를) 추출하려면 원래 설치 패키지를 압축하지 않고 추적하지 않아야 합니다.
1. [!DNL uninstall.sh]을(를) 실행하고 화면에 표시되는 안내를 따릅니다.

## 방법 2

1. 다음을 사용하여 이미지 렌더링을 중지합니다.

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. 시스템에서 ImageRendering을 제거합니다. 사용하는 명령은 시스템에 따라 다릅니다.
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. 2단계에서 제거되지 않은 모든 디렉토리 또는 파일을 삭제합니다.

