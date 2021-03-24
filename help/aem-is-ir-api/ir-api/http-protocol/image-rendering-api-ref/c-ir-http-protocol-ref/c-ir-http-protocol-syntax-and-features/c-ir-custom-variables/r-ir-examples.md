---
description: 이 예제에서는 [이미지 제공]을 사용하여 객체에 색상을 적용하고 비네팅 집합 중 하나에 사용자 정의 텍스트를 포함하는 데모를 적용합니다.
solution: Experience Manager
title: 예제
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---


# 예제{#examples}

이 예제에서는 [이미지 제공]을 사용하여 객체에 색상을 적용하고 비네팅 집합 중 하나에 사용자 정의 텍스트를 포함하는 데모를 적용합니다.

IR 변수는 비네팅, 로고 이미지 및 사용자 정의 텍스트를 식별하는 데 사용됩니다.

재료 카탈로그 `myCat`의 비네팅 맵에 있는 *template*&#x200B;이라는 레코드에 있는 `vignette::Modifier` 필드에 다음이 포함됩니다.

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

사용할 모든 비네팅은 재료 카탈로그 `myCat`의 비네팅 맵에 나열됩니다.

이제 클라이언트는 기본 이미지를 검색하기 위해 다음 요청을 수행할 수 있습니다(템플릿 시작 부분에 정의된 변수를 사용합니다).

[!DNL `https://server/myCat/template`]

다음 요청은 렌더링할 특정 컨텐츠를 지정합니다.

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

`text=` 이미지 제공 명령에 대한 자세한 내용은 이미지 제공 설명서를 참조하십시오.
