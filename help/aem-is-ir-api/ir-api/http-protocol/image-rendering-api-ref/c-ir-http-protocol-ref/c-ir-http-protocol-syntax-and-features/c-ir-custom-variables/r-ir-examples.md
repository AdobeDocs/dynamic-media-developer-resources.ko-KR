---
title: 예제
description: 이 예제에서는 [이미지 제공]을 사용하여 개체에 색상을 지정하고 사용자 정의 텍스트가 포함된 데모를 비네팅 세트 중 하나에 적용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# 예제{#examples}

이 예제에서는 [이미지 제공]을 사용하여 개체에 색상을 지정하고 사용자 정의 텍스트가 포함된 데모를 비네팅 세트 중 하나에 적용합니다.

IR 변수는 비네팅, 로고 이미지 및 사용자 지정 텍스트를 식별하는 데 사용됩니다.

다음 `vignette::Modifier` 이름이 지정된 레코드의 필드 *템플릿* 재료 카탈로그의 비네팅 맵에서 `myCat` 에는 다음 항목이 포함되어 있습니다.

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

사용된 모든 비네팅은 재료 카탈로그의 비네팅 맵에 나열됩니다 `myCat`.

이제 클라이언트는 다음 요청을 수행하여 기본 이미지를 검색할 수 있습니다(템플릿의 시작 부분에 정의된 변수를 사용).

[!DNL `https://server/myCat/template`]

다음 요청은 렌더링할 특정 콘텐츠를 지정합니다.

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

이미지 서비스에 대한 자세한 내용은 이미지 제공 설명서 를 참조하십시오 `text=` 명령.
