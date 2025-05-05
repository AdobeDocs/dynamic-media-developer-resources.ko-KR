---
title: 명령 매크로
description: 명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 명령 매크로{#command-macros}

명령 매크로는 명령 집합에 대해 명명된 단축키를 제공합니다.

`$ *[!DNL name]*$`

**&#x200B; *[!DNL name]* &#x200B;** 이름 입력

매크로는 별도의 매크로 정의 파일로 정의되며, 재료 카탈로그 또는 기본 카탈로그에 첨부할 수 있습니다.

*[!DNL name]*&#x200B;은(는) 대/소문자를 구분하지 않으며 ASCII 문자, 숫자 , &#39;-&#39;, &#39;_&#39; 및 &#39;.&#39;의 조합으로 구성될 수 있습니다. 자.

요청의 &#39;?&#39; 뒤에 있는 곳이나 `vignette::Modifier` 필드 내에 있는 모든 곳에서 매크로를 호출합니다. 매크로는 하나 이상의 이미지 렌더링 명령만 나타낼 수 있으며 &#39;&amp;&#39; 구분 기호를 사용하여 다른 명령과 구분해야 합니다.

매크로 호출은 구문 분석 중에 대체 문자열로 조기에 대체됩니다. 매크로 내의 명령은 요청에서 매크로 호출 전에 발생한 경우 요청에서 동일한 명령을 재정의합니다. 이 워크플로는 요청의 위치에 관계없이 요청 문자열의 명령이 `vignette::Modifier` 문자열의 명령을 재정의하는 `vignette::Modifier`과(와) 다릅니다.

명령 매크로에는 인수 값을 사용할 수 없지만 사용자 지정 변수를 사용하여 요청에서 매크로로 값을 전달할 수 있습니다.

매크로가 중첩되어 있지 않을 수 있습니다.

**예**

매크로는 동일한 명령 또는 특성을 다른 렌더링된 이미지에 적용하는 경우에 유용합니다.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

일반 속성에 대해 매크로를 정의할 수 있습니다.

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

매크로는 다음과 같이 사용됩니다.

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

세 번째 요청에 대해 `qlt=`이(가) 다르므로 매크로가 호출된 후 소프트웨어가 값을 재정의합니다(`qlt=` *before* `$render$`을(를) 지정하는 것은 효과가 없음).

**참고 항목**

`catalog::MacroFile`, `catalog::Modifier`, 매크로 정의 참조

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
