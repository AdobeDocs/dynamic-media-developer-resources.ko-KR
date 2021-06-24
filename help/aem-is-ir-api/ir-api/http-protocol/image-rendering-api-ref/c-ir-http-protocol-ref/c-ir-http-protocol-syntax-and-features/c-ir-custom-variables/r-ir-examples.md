---
description: 이 예제에서는 [이미지 제공]을 사용하여 개체에 색상을 지정하고 사용자 정의 텍스트가 포함된 데모를 비네팅 세트 중 하나에 적용합니다.
solution: Experience Manager
title: 예제
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 1%

---

# 예제{#examples}

이 예제에서는 [이미지 제공]을 사용하여 개체에 색상을 지정하고 사용자 정의 텍스트가 포함된 데모를 비네팅 세트 중 하나에 적용합니다.

IR 변수는 비네팅, 로고 이미지 및 사용자 지정 텍스트를 식별하는 데 사용됩니다.

재료 카탈로그 `myCat`의 비네팅 맵에 있는 *template*&#x200B;라는 레코드의 `vignette::Modifier` 필드에는 다음 내용이 포함됩니다.

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

사용할 모든 비네팅은 재료 카탈로그 `myCat`의 비네팅 맵에 나열되어 있습니다.

이제 클라이언트가 기본 이미지를 검색하도록 다음 요청을 수행할 수 있습니다(템플릿 시작 부분에 정의된 변수를 사용).

[!DNL `https://server/myCat/template`]

다음 요청은 렌더링할 특정 콘텐츠를 지정합니다.

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

이미지 제공 `text=` 명령에 대한 자세한 내용은 이미지 제공 설명서 를 참조하십시오.
