---
title: Linux® 및 Solaris™에서 제거
description: 다음 지침에 따라 Linux® 또는 Solaris™ 시스템에서 이미지 렌더링을 제거합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 5%

---

# Linux® 및 Solaris™에서 제거{#uninstalling-on-linux-and-solaris}

다음 지침에 따라 Linux® 또는 Solaris™ 시스템에서 이미지 렌더링을 제거합니다. 사용할 수 있는 방법에는 두 가지가 있습니다. 다음 중 하나를 수행하십시오.

## 방법 1

1. 찾기 [!DNL uninstall.sh].

   ImageRendering이 설치된 디렉터리에 있습니다. 이 디렉토리를 제거한 경우 원래 설치 패키지를 압축하지 않고 추출하지 않아야 합니다 [!DNL uninstall.sh].
1. 실행 [!DNL uninstall.sh] 화면의 지시를 따릅니다.

## 방법 2

1. ImageRendering을 다음으로 중지합니다.

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. 시스템에서 ImageRendering을 제거합니다. 사용하는 명령은 시스템에 따라 다릅니다.
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. 2단계에서 제거되지 않은 디렉토리 또는 파일을 삭제합니다.

