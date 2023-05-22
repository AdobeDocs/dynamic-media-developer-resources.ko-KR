---
description: 명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다.
solution: Experience Manager
title: 명령 매크로
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# 명령 매크로{#command-macros}

명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다.

매크로는 이미지 카탈로그나 기본 카탈로그에 첨부할 수 있는 별도의 매크로 정의 파일로 정의됩니다.

매크로는 요청의 어디에서나 &#39;?&#39; 뒤에 호출할 수 있고 `catalog::Modifier` 필드. 매크로는 하나 이상의 완전한 이미지 제공 명령만 나타낼 수 있으므로 &#39;&amp;&#39; 구분 기호로 묶어야 합니다(수정자 문자열의 시작 또는 끝에 있는 경우 제외).

매크로 호출은 구문 분석 중에 대체 문자열로 조기에 대체됩니다. 매크로 내의 명령은 요청에서 매크로 호출 전에 발생할 경우 요청에서 동일한 명령을 재정의합니다. 이 은(는) 과(와) 다릅니다. `catalog::Modifier`: 요청 문자열의 명령이 항상 의 명령을 재정의합니다. `catalog::Modifier` 문자열(요청에서 위치에 상관없이).

매크로는 다음과 같은 제한으로 중첩될 수 있습니다. 매크로 정의를 구문 분석할 때 동일한 매크로 정의 파일에서 앞에 나타나거나 기본 매크로 정의 파일에 포함된 매크로에 대한 정의를 배치하는 방식으로 매크로가 이미 정의된 경우에만 매크로를 호출할 수 있습니다.

매크로는 동일한 특성을 다른 이미지에 적용할 경우에 유용합니다.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

공통 속성에 대한 매크로를 정의할 수 있습니다.

`view wid=240&fmt=pdf&imageRes=300`

매크로는 다음과 같이 사용됩니다.

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

다음 이후 `wid=` 은 세 번째 요청에 대해 다르므로 값을 재정의합니다. *이후* 매크로가 호출됩니다(지정) `wid=`*다음 이전* `$view$` 에는 영향이 없습니다).

+ [name](r-name.md)
