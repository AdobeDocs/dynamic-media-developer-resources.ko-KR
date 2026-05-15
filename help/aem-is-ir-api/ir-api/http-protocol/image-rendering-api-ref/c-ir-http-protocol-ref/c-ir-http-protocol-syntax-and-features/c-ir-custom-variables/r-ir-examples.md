---
title: 예제
description: 이 예제에서는 이미지 제공 을 사용하여 오브젝트를 색상화하고 비네팅 세트 중 하나에 사용자 지정 텍스트를 포함하는 데칼을 적용합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
TQID: 'https://experienceleague.adobe.com/GMzKDuP-wzTrPJQbxpXc0M08BjCQdWCkGo5jOUiWipU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 1%

---

# 예제{#examples}

이 예제에서는 이미지 제공 을 사용하여 오브젝트를 색상화하고 비네팅 세트 중 하나에 사용자 지정 텍스트를 포함하는 데칼을 적용합니다.

IR 변수는 비네팅, 로고 이미지 및 사용자 지정 텍스트를 식별하는 데 사용됩니다.

재질 카탈로그 `myCat`의 비네팅 맵에서 이름이 *template*&#x200B;인 레코드의 `vignette::Modifier` 필드에 다음이 포함되어 있습니다.

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

사용된 모든 비네팅은 재질 카탈로그 `myCat`의 비네팅 맵에 나열됩니다.

이제 클라이언트가 기본 이미지 검색을 위해 다음 요청을 수행할 수 있습니다(템플릿 시작 부분에 정의된 변수 사용).

[!DNL `https://server/myCat/template`]

다음 요청은 렌더링할 특정 콘텐츠를 지정합니다.

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

이미지 제공 `text=` 명령에 대한 자세한 내용은 이미지 제공 설명서를 참조하십시오.
