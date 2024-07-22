---
title: 사용자 지정 변수
description: 요청 및 비네팅 수정자 문자열의 쿼리 부분은 사용자 정의 변수를 포함할 수 있다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# 사용자 지정 변수{#custom-variables}

요청 및 비네팅::수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - 변수 이름입니다. `$`을(를) 제외하고 알파, 숫자 및 안전 문자의 조합으로 구성될 수 있습니다.

`[!DNL value]` - 변수를 설정할 값(문자열).

변수는 위의 구문을 사용하여 다른 서버 명령과 유사하게 정의됩니다. 변수를 참조하려면 먼저 정의해야 합니다. `vignette::Modifier`에 정의된 변수는 URL 요청에서 참조할 수 있습니다.

>[!NOTE]
>
>`[!DNL value]`은(는) 안전한 HTTP 전송을 위해 단일 패스 URL로 인코딩되어야 합니다. `[!DNL value]`이(가) HTTP를 통해 다시 전송되는 경우 이중 인코딩이 필요합니다. 이 상황은 `[!DNL value]`이(가) 중첩된 외래 요청으로 대체되는 경우입니다.

명령 값의 앞과 뒤에 있는 변수 이름(`$`)을 포함하여 변수를 참조합니다. 예를 들어 명령 이름 다음에 오는 `=`과(와) 후속 `&` 또는 요청 끝 사이에 있을 수 있습니다. 서버는 이러한 각 `$ [!DNL name]$` 항목을 `[!DNL string]`(으)로 대체합니다. 명령 이름(명령의 등호 앞) 및 요청의 경로 부분에서 `$ [!DNL name]$`의 발생 항목에 대체가 발생하지 않습니다.

사용자 지정 변수는 중첩되지 않을 수 있습니다. `[!DNL string]` 내의 모든 `$ [!DNL name]$` 항목은 대체되지 않습니다. 예를 들어 요청 조각 `$var2=apple&$var1=my$var2$tree&text=$var1$`은(는) `text=my$var2$tree`(으)로 확인됩니다.

`$`은(는) 예약된 문자가 아닙니다. 요청에서 다른 문자가 발생할 수 있습니다. 예를 들어 `wid=`에 숫자 인수가 필요하므로 `src=my$texture$file.tif`은(는) 올바른 명령이지만 `[!DNL my$texture$file.tif]`(이)라는 재질 카탈로그 항목 또는 텍스처 파일이 있다고 가정할 경우 `wid=$number$`은(는) 그렇지 않습니다.
