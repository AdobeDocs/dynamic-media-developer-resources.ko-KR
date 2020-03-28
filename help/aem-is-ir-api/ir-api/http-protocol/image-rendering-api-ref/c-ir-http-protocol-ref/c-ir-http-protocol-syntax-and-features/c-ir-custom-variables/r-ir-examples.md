---
description: 이 예에서는 이미지 제공을 사용하여 개체에 색상을 적용하고 비네팅 세트 중 하나에서 사용자 정의 텍스트가 포함된 데모를 적용합니다.
seo-description: 이 예에서는 이미지 제공을 사용하여 개체에 색상을 적용하고 비네팅 세트 중 하나에서 사용자 정의 텍스트가 포함된 데모를 적용합니다.
seo-title: 예제
solution: Experience Manager
title: 예제
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# 예제{#examples}

이 예에서는 이미지 제공을 사용하여 개체에 색상을 적용하고 비네팅 세트 중 하나에서 사용자 정의 텍스트가 포함된 데모를 적용합니다.

IR 변수는 비네팅, 로고 이미지 및 사용자 정의 텍스트를 식별하는 데 사용됩니다.

자재 카탈로그의 비네팅 맵에 있는 `vignette::Modifier` 템플릿이라는 *레코드의 필드에는* `myCat` 다음 내용이 포함되어 있습니다.

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

사용할 모든 비네팅은 재료 카탈로그의 비네팅 맵에 나열되어 `myCat`있습니다.

클라이언트는 이제 기본 이미지를 검색하기 위해 다음 요청을 수행할 수 있습니다(템플릿 시작 시 정의된 변수 사용).

[!DNL `https://server/myCat/template`]

다음 요청은 렌더링할 특정 컨텐츠를 지정합니다.

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

이미지 제공 `text=` 명령에 대한 자세한 내용은 이미지 제공 설명서를 참조하십시오.
