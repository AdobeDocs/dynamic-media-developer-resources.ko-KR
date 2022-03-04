---
title: 사용자 지정 변수
description: 요청 및 비네팅 수정자 문자열의 쿼리 부분에는 사용자 정의 변수가 포함될 수 있습니다.
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

요청 및 비네트의 쿼리 부분::수정자 문자열에는 사용자 정의 변수가 포함될 수 있습니다.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - 변수 이름. 영문자, 숫자 및 안전 문자의 조합으로 구성될 수 있습니다(제외). `$`.

`[!DNL value]` - 변수를 설정할 값(문자열).

변수는 위의 구문을 사용하여 다른 서버 명령과 유사하게 정의됩니다. 변수를 참조하려면 먼저 변수를 정의해야 합니다. 에 정의된 변수 `vignette::Modifier` 는 URL 요청에서 참조되고 반대로 참조할 수 있습니다.

>[!NOTE]
>
>`[!DNL value]` 안전한 HTTP 전송을 위해 단일 전달 URL로 인코딩되어야 합니다. 이중 인코딩이 필요한 경우 `[!DNL value]` 는 HTTP를 통해 다시 전송됩니다. 이 상황은 다음과 같습니다 `[!DNL value]` 는 중첩된 외부 요청으로 대체됩니다.

변수 이름(선행 및 후행 문자로 묶음)을 포함하여 변수를 참조합니다 `$`)을 명령 값의 어느 곳에서든 사용할 수 있습니다. 예를 들어 다음 사이 `=`  명령 이름과 다음에 `&` 또는 요청의 끝. 서버는 이러한 발생 항목을 `$ [!DNL name]$` with `[!DNL string]`. 어떤 경우에도 대체가 발생하지 않습니다 `$ [!DNL name]$` 명령 이름(명령의 등호 전) 및 요청의 경로 부분에서

사용자 지정 변수는 중첩되지 않을 수 있습니다. 모든 발생 횟수 `$ [!DNL name]$` within `[!DNL string]` 은 대체되지 않습니다. 예를 들어 요청 조각이 있습니다 `$var2=apple&$var1=my$var2$tree&text=$var1$` 확인됨 `text=my$var2$tree`.

`$` 는 예약된 문자가 아닙니다. 이 문제는 요청에서 달리 발생할 수 있습니다. 예, `src=my$texture$file.tif` 는 유효한 명령입니다(이름이 `[!DNL my$texture$file.tif]` 존재) `wid=$number$` 아님 `wid=` 에는 숫자 인수가 필요합니다.
