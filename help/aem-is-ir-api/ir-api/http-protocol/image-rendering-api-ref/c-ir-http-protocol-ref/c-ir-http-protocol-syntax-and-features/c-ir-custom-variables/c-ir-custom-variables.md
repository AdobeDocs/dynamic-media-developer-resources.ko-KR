---
description: 요청 및 비네팅 수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.
seo-description: 요청 및 비네팅 수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.
seo-title: 사용자 지정 변수
solution: Experience Manager
title: 사용자 지정 변수
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# 사용자 지정 변수{#custom-variables}

요청 및 비네팅::수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **변수 이름. &#39;$.&#39;을(를) 제외하고 알파, 숫자 및 안전 문자의 조합으로 구성할 수 있습니다.

** *[!DNL value]* ** 변수를 설정할 값(문자열)입니다.

변수는 위의 구문을 사용하여 다른 서버 명령과 유사하게 정의됩니다. 변수를 참조하려면 먼저 정의해야 합니다. `vignette::Modifier`에 정의된 변수는 URL 요청에서 참조할 수 있으며 그 반대의 경우도 마찬가지입니다.

>[!NOTE]
>
>*[!DNL value]* 안전한 HTTP 전송을 위해 단일 패스 URL로 인코딩되어야 합니다. *[!DNL value]*&#x200B;이(가) HTTP를 통해 다시 전송되는 경우 이중 인코딩이 필요합니다. 이것은 *[!DNL value]*&#x200B;이(가) 중첩된 외부 요청으로 대체되는 경우입니다.

변수는 명령 값에 변수 이름(행간 및 후행 $)을 포함시켜 참조합니다. 예를 들어, 명령 이름 뒤에 오는 &#39;=&#39; 사이 및 후속 &#39;&amp;&#39; 또는 요청의 끝 사이의 경우입니다. 이 서버는 이러한 각 $ *[!DNL name]*$ 을 *[!DNL string]*&#x200B;으로 대체합니다. 명령 이름에 $ *[!DNL name]*$ 이 있는 경우(명령 등호 전) 및 요청의 경로 부분에 대체 요소가 발생하지 않습니다.

사용자 지정 변수는 중첩될 수 없습니다. *[!DNL string]* 내에 있는 $ *[!DNL name]*$ 의 모든 항목은 대체되지 않습니다. 예를 들어 요청 조각 `$var2=apple&$var1=my$var2$tree&text=$var1$`은 `text=my$var2$tree`으로 확인됩니다.

$ 는 예약된 문자가 아닙니다.이 문제는 요청에서 다르게 발생할 수 있습니다. 예를 들어 `wid=`에는 숫자 인수가 필요하므로 `src=my$texture$file.tif`은(는) [!DNL my$texture$file.tif]이라는 재료 카탈로그 항목 또는 텍스처 파일이 있다고 가정할 때) 유효한 명령이지만 `wid=$number$`는 그렇지 않습니다.
