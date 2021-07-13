---
description: 속성 데이터는 하나 이상의 속성을 나타내는 텍스트 문자열로 구성됩니다.
solution: Experience Manager
title: 속성 데이터
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# 속성 데이터{#property-data}

속성 데이터는 하나 이상의 속성을 나타내는 텍스트 문자열로 구성됩니다.

속성은 속성 이름과 속성 값으로 구성되며 = 로 구분됩니다.

여러 속성은 줄 구분자로 구분되며, 이 구분자는 `??` 또는 `<CR><LF>`일 수 있습니다. 전체 속성 데이터 문자열이 따옴표로 묶이지 않으면 서버는 데이터를 클라이언트로 전송하기 전에 `??` 의 각 항목을 `<CR><LF>` 로 바꿉니다. 속성 이름은 문자, 숫자, &#39;.&#39;, &#39;-&#39; 및 &#39;_&#39;로 구성될 수 있습니다. 속성 이름은 대/소문자를 구분하지 않습니다.

속성 값에는 라인 구분자를 포함하지 않아야 합니다.

속성 데이터에 적용되는 추가 규칙은 [텍스트 문자열](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)을 참조하십시오.
