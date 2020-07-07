---
description: 요청 및 비네팅 수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.
seo-description: 요청 및 비네팅 수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.
seo-title: 사용자 지정 변수
solution: Experience Manager
title: 사용자 지정 변수
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Custom variables{#custom-variables}

요청 및 비네팅::수정자 문자열에는 사용자 정의 변수가 포함될 수 있습니다.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **변수 이름. &#39;$.&#39;을(를) 제외한 모든 알파, 숫자 및 안전 문자 조합으로 구성될 수 있습니다.

** *[!DNL value]* ** 변수를 설정할 값(문자열)입니다.

변수는 위의 구문을 사용하여 다른 서버 명령과 유사하게 정의됩니다. 변수를 참조하려면 먼저 정의해야 합니다. 에서 정의된 변수는 URL 요청에서 참조될 `vignette::Modifier` 수 있고 그 반대의 경우도 마찬가지입니다.

>[!NOTE]
>
>*[!DNL value]* 안전한 HTTP 전송을 위해 단일 패스 URL로 인코딩되어야 합니다. HTTP를 통해 다시 전송되는 경우 이중 인코딩 *[!DNL value]* 이 필요합니다. 이것은 중첩된 외부 요청 *[!DNL value]* 으로 대체되는 경우입니다.

변수는 명령 값 내에 변수 이름(앞과 뒤에 있는 $)을 삽입하여 참조합니다. 예를 들어, 명령 이름 뒤에 있는 &#39;=&#39; 사이에, 그 뒤의 &#39;&amp;&#39; 또는 요청의 끝 사이에 있습니다. 서버는 이러한 $ *[!DNL name]*$ 의 발생을 $$로 *[!DNL string]*&#x200B;대체합니다. 명령 이름에 $ *[!DNL name]*$(명령의 등호 전) 발생 및 요청의 경로 부분에 대체 요소가 발생하지 않습니다.

사용자 지정 변수는 중첩될 수 없습니다. Any occurrence of $ *[!DNL name]*$ within *[!DNL string]* are not replaced. 예를 들어 요청 조각이 로 `$var2=apple&$var1=my$var2$tree&text=$var1$` 확인됩니다 `text=my$var2$tree`.

$ is not reserved character; 이 문제는 요청에서 달리 발생할 수 있습니다. 예를 들어 `src=my$texture$file.tif` 는 숫자 인수가 필요하므로 은 아니지만 유효한 명령(이름이 지정된 재료 카탈로그 항목 또는 텍스처 파일 [!DNL my$texture$file.tif] 이 있다고 가정함) `wid=$number$` `wid=` 입니다.
