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

`[!DNL name]` - 변수 이름. 알파, 숫자 및 안전 문자를 조합하여 사용할 수 있습니다. 단, `$`.

`[!DNL value]` - 변수를 설정할 값(문자열).

변수는 위의 구문을 사용하여 다른 서버 명령과 유사하게 정의됩니다. 변수를 참조하려면 먼저 정의해야 합니다. 에 정의된 변수 `vignette::Modifier` 는 URL 요청에서 참조될 수 있으며, 반대로 참조될 수 있습니다.

>[!NOTE]
>
>`[!DNL value]` 안전한 HTTP 전송을 위해 단일 패스 URL로 인코딩해야 합니다. 다음의 경우 이중 인코딩이 필요합니다. `[!DNL value]` 은 HTTP를 통해 재전송됩니다. 이 상황은 다음과 같습니다. `[!DNL value]` 는 중첩된 외부 요청으로 대체됩니다.

변수 이름(선행 및 후행으로 둘러싸인 변수 포함)을 사용하여 변수를 참조합니다. `$`) 명령 값의 모든 위치. 예를 들어 다음 사이 `=`  다음 명령 이름 및 후속 명령 `&` 또는 요청의 끝. 서버는 이러한 각 발생 항목을 `$ [!DNL name]$` 포함 `[!DNL string]`. 다음 발생 항목에는 대체가 발생하지 않습니다. `$ [!DNL name]$` 명령 이름(명령의 등호 앞) 및 요청의 경로 부분에서 사용할 수 있습니다.

사용자 지정 변수는 중첩되지 않을 수 있습니다. 다음 중 발생 횟수 `$ [!DNL name]$` 다음 범위 내 `[!DNL string]` 은 대체되지 않습니다. 예: 요청 조각 `$var2=apple&$var1=my$var2$tree&text=$var1$` 다음으로 확인됨: `text=my$var2$tree`.

`$` 은(는) 예약된 문자가 아닙니다. 요청에서 달리 발생할 수 있습니다. 예를 들어, `src=my$texture$file.tif` 은 유효한 명령입니다(라는 재료 카탈로그 항목 또는 텍스처 파일이 있다고 가정). `[!DNL my$texture$file.tif]` 존재함), while `wid=$number$` 은(는) 다음과 같지 않습니다. `wid=` 에는 숫자 인수가 필요합니다.
