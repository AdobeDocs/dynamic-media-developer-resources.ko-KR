---
description: 명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다.
seo-description: 명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다.
seo-title: 명령 매크로
solution: Experience Manager
title: 명령 매크로
topic: Scene7 Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 4169757880407b62addd0a70ef1807d8b195820b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# 명령 매크로{#command-macros}

명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다.

매크로는 이미지 카탈로그 또는 기본 카탈로그에 첨부할 수 있는 별도의 매크로 정의 파일에 정의됩니다.

매크로는 &#39;?&#39; 이후 요청과 `catalog::Modifier` 필드 내의 어느 곳에서든 호출할 수 있습니다. 매크로는 하나 이상의 완전한 이미지 제공 명령만 나타낼 수 있으므로 &#39;&amp;&#39; 구분 문자로 둘러싸야 합니다(수정자 문자열의 시작 또는 끝에 있는 경우 제외).

구문 분석 중에는 일찍 매크로 함수가 대체 문자열로 대체됩니다. 매크로 내의 명령은 요청에서 매크로 호출 전에 발생하는 경우 요청에서 동일한 명령을 덮어씁니다. 이것은 `catalog::Modifier`과 다릅니다. 요청 문자열의 명령은 항상 요청의 위치에 관계없이 `catalog::Modifier` 문자열의 명령을 재정의합니다.

매크로가 중첩될 수 있으며 다음과 같은 제한이 있습니다.매크로 정의를 파싱할 때, 같은 매크로 정의 파일에 앞쪽을 표시하거나 기본 매크로 정의 파일에 포함된 매크로의 정의를 배치하여 매크로 정의를 이미 정의한 경우에만 매크로를 호출할 수 있습니다.

매크로는 동일한 특성을 다른 이미지에 적용할 때 유용합니다.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

공통 속성에 대한 매크로를 정의할 수 있습니다.

`view wid=240&fmt=pdf&imageRes=300`

매크로를 다음과 같이 사용합니다.

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

`wid=`은(는) 세 번째 요청에 대해 다르므로, 매크로가 호출된 후 *after* 값을 무시하면 됩니다(*`$view$`&lt;a5/> 에는 아무런 영향이 없습니다.).`wid=`*

+ [name](r-name.md)
