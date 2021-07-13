---
description: 요청 및 비네팅 수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.
solution: Experience Manager
title: 사용자 지정 변수
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# 사용자 지정 변수{#custom-variables}

요청 및 비네트의 쿼리 부분::수정자 문자열에는 사용자 정의 변수가 포함될 수 있습니다.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **변수 이름. &#39;$&#39;을(를) 제외한 모든 알파벳, 숫자 및 안전 문자 조합으로 구성될 수 있습니다.

** *[!DNL value]* ** 변수를 설정할 값(문자열)입니다.

변수는 위의 구문을 사용하여 다른 서버 명령과 유사하게 정의됩니다. 변수를 참조하려면 먼저 변수를 정의해야 합니다. `vignette::Modifier`에 정의된 변수는 URL 요청에서 참조할 수 있고 그 반대의 경우도 가능합니다.

>[!NOTE]
>
>*[!DNL value]* 안전한 HTTP 전송을 위해 단일 전달 URL로 인코딩되어야 합니다. HTTP를 통해 *[!DNL value]*&#x200B;을 다시 전송하는 경우 이중 인코딩이 필요합니다. 이는 *[!DNL value]*&#x200B;이 중첩된 외부 요청으로 대체되는 경우입니다.

변수 이름(선행 및 후행 $)으로 묶은)을 명령 값에 포함하여 변수를 참조합니다. 예를 들어, 명령 이름 뒤에 &#39;=&#39;가 있으면 후속 &#39;&amp;&#39; 또는 요청의 끝 사이에 서버는 이러한 $ *[!DNL name]*$ 의 각 항목을 *[!DNL string]* 로 바꿉니다. 명령 이름에 $ *[!DNL name]*$ 이(가) 있을 때(명령 등호가 되기 전에), 그리고 요청의 경로 부분에서 대체 작업이 발생하지 않습니다.

사용자 지정 변수는 중첩되지 않을 수 있습니다. *[!DNL string]* 내에서 $ *[!DNL name]*$ 의 모든 발생 항목이 대체되지 않습니다. 예를 들어 요청 조각 `$var2=apple&$var1=my$var2$tree&text=$var1$`이 `text=my$var2$tree`로 확인됩니다.

$ 는 예약된 문자가 아닙니다. 이 문제는 요청에서 달리 발생할 수 있습니다. 예를 들어 `src=my$texture$file.tif`은(는) [!DNL my$texture$file.tif]이라는 이름의 재료 카탈로그 항목이나 텍스처 파일이 있다고 가정할 때) 유효한 명령이지만 `wid=$number$`는 숫자 인수가 필요하므로 이 아닌 것입니다.`wid=`
