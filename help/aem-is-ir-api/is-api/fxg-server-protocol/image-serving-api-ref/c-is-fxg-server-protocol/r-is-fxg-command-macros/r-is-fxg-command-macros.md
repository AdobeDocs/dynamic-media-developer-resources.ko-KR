---
description: 명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다.
solution: Experience Manager
title: 명령 매크로
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# 명령 매크로{#command-macros}

명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다.

매크로는 별도의 매크로 정의 파일로 정의되며 이미지 카탈로그 또는 기본 카탈로그에 첨부할 수 있습니다.

매크로는 &#39;?&#39; 뒤에 있는 요청이나 `catalog::Modifier` 필드 내의 어느 곳에서든 호출될 수 있습니다. 매크로는 하나 이상의 완전한 이미지 제공 명령만 나타낼 수 있으므로 &#39;&amp;&#39; 구분 기호로 묶어야 합니다(보조 문자열의 시작 또는 끝에 있는 경우 제외).

구문 분석 중에는 매크로 함수가 먼저 대체 문자열로 대체됩니다. 매크로 내의 명령은 요청에서 매크로 호출 전에 발생할 경우 요청에서 동일한 명령을 재정의합니다. 이는 `catalog::Modifier`과 다릅니다. 여기서 요청 문자열의 명령은 요청의 위치와 관계없이 항상 `catalog::Modifier` 문자열의 명령을 재정의합니다.

매크로가 중첩될 수 있으며 다음과 같은 제한 사항이 있습니다. 매크로는 매크로 정의가 구문 분석될 때 이미 정의된 경우 같은 매크로 정의 파일에 앞쪽으로 나타나거나 기본 매크로 정의 파일에 해당 포함 매크로의 정의를 배치하여 호출할 수 있습니다.

매크로는 동일한 속성을 다른 이미지에 적용해야 하는 경우에 유용합니다.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

공통 특성에 대한 매크로를 정의할 수 있습니다.

`view wid=240&fmt=pdf&imageRes=300`

매크로는 다음과 같이 사용됩니다.

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

`wid=`은(는) 세 번째 요청에 대해 다르므로, *after* 값을 재정의하면 됩니다(*`$view$` 전에`wid=`*&#x200B;을 지정하면 영향을 받지 않습니다.).

+ [name](r-name.md)
