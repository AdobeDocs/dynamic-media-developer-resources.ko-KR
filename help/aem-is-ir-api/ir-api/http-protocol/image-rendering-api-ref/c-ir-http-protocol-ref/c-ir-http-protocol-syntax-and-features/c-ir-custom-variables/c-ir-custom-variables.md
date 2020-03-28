---
description: 요청 및 비네팅 수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.
seo-description: 요청 및 비네팅 수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.
seo-title: 사용자 지정 변수
solution: Experience Manager
title: 사용자 지정 변수
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Custom variables{#custom-variables}

요청 및 비네팅::수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **변수 이름. &#39;$.&#39;을(를) 제외하고 알파, 숫자 및 안전 문자의 조합으로 구성될 수 있습니다.

** *[!DNL value]* ** 변수를 설정할 값(문자열)입니다.

변수는 위의 구문을 사용하여 다른 서버 명령과 유사하게 정의됩니다. 변수를 참조하려면 먼저 정의해야 합니다. 에서 정의된 변수는 URL 요청에서 참조되거나 그 반대로 참조할 `vignette::Modifier` 수 있습니다.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>*[!DNL value]* 안전한 HTTP 전송을 위해 단일 패스 URL로 인코딩되어야 합니다. HTTP를 통해 다시 *[!DNL value]* 전송하는 경우 이중 인코딩이 필요합니다. 중첩 외부 요청으로 대체되는 *[!DNL value]* 경우입니다.

변수는 변수 이름(행간 및 후행 $)을 명령 값에 포함시켜 참조합니다. 예를 들어, 명령 이름 뒤에 오는 &#39;=&#39;와 후속 &#39;&amp;&#39; 또는 요청의 끝 사이에 있습니다. 서버는 이러한 $ *[!DNL name]*$ 의 발생을 각각 $$ 으로 *[!DNL string]*&#x200B;대체합니다. 명령 이름(명령의 등호 전)과 요청의 경로 부분에서 $ *[!DNL name]*$ 발생 시 대체 요소가 발생하지 않습니다.

사용자 지정 변수는 중첩될 수 없습니다. $ *[!DNL name]*$ 내에서 발생하는 모든 항목은 *[!DNL string]* 대체되지 않습니다. 예를 들어 요청 조각이 로 `$var2=apple&$var1=my$var2$tree&text=$var1$` 확인됩니다 `text=my$var2$tree`.

$ is not reserved character;이 경우 요청에서 다르게 발생할 수 있습니다. 예를 들어 `src=my$texture$file.tif` 는 유효한 명령입니다(이름이 [!DNL my$texture$file.tif] 지정된 재료 카탈로그 항목 또는 텍스처 파일이 있다고 가정할 경우). 단, 숫자 인수가 필요하므로 `wid=$number$` 그렇지 않습니다 `wid=` .
