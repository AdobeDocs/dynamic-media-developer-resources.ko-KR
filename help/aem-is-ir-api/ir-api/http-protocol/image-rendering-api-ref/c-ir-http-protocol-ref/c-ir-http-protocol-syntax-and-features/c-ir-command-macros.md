---
description: 명령 매크로는 명령 세트에 대해 명명된 단축키를 제공합니다.
seo-description: 명령 매크로는 명령 세트에 대해 명명된 단축키를 제공합니다.
seo-title: 명령 매크로 *
solution: Experience Manager
title: 명령 매크로 *
topic: Scene7 Image Serving - Image Rendering API
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 명령 매크로 *{#command-macros}

명령 매크로는 명령 세트에 대해 명명된 단축키를 제공합니다.

`$ *[!DNL name]*$`

** *[!DNL name]* ** 매크로 이름

매크로는 별도의 매크로 정의 파일에 정의되며, 이를 재료 카탈로그 또는 기본 카탈로그에 첨부할 수 있습니다.

*[!DNL name]* 은 대/소문자를 구분하지 않으며 ASCII 문자, 숫자, &#39;-&#39;, &#39;_&#39; 및 &#39;.&#39; 조합으로 구성할 수 있습니다. 문자.

&#39;?&#39; 뒤에 있는 요청이나 `vignette::Modifier` 필드 내의 아무 곳에서나 매크로를 호출합니다. 매크로는 하나 이상의 전체 이미지 렌더링 명령만 나타낼 수 있으며 &#39;&amp;&#39; 구분 기호가 있는 다른 명령과 구분해야 합니다.

구문 분석 중에는 일찍 매크로 함수가 대체 문자열로 대체됩니다. 매크로 내의 명령은 요청에서 매크로 호출 전에 발생하는 경우 요청에서 동일한 명령을 덮어씁니다. 이것은 `vignette::Modifier`요청에서 위치에 관계없이 요청 문자열의 명령은 항상 `vignette::Modifier` 문자열의 명령을 재정의합니다.

명령 매크로에는 인수 값을 사용할 수 없지만 사용자 지정 변수를 사용하여 요청의 값을 매크로로 전달할 수 있습니다.

매크로가 중첩될 수 없습니다.

**예**

매크로는 다른 렌더링된 이미지에 동일한 명령이나 속성을 적용할 때 유용합니다.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

일반적인 속성에 대한 매크로를 정의할 수 있습니다.

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

매크로는 다음과 같이 사용됩니다.

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

세 번째 요청에 `qlt=` 대해 다르므로, 매크로를 호출한 후 값을 재정의하면 됩니다( `qlt=`*그 전에&#x200B;*지정하면`$render$`아무런 영향이 없습니다).

**참조**

`catalog::MacroFile`, `catalog::Modifier`, 매크로 정의 참조

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

