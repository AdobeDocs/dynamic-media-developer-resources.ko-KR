---
description: 속성 데이터는 하나 이상의 속성을 나타내는 텍스트 문자열로 구성됩니다.
seo-description: 속성 데이터는 하나 이상의 속성을 나타내는 텍스트 문자열로 구성됩니다.
seo-title: 속성 데이터
solution: Experience Manager
title: 속성 데이터
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# 속성 데이터{#property-data}

속성 데이터는 하나 이상의 속성을 나타내는 텍스트 문자열로 구성됩니다.

속성은 속성 이름과 속성 값으로 구성되며 = 로 구분됩니다.

여러 속성은 행 구분 기호로 구분되어 있으며, 이 구분 기호는 `??` 또는 `<CR><LF>`일 수 있습니다. 전체 속성 데이터 문자열을 따옴표로 묶지 않으면 서버는 데이터를 클라이언트에 전송하기 전에 `??`의 각 항목을 `<CR><LF>`으로 바꿉니다. 속성 이름은 문자, 숫자, &#39;.&#39;, &#39;-&#39; 및 &#39;_&#39;로 구성될 수 있습니다. 속성 이름은 대/소문자를 구분하지 않습니다.

속성 값은 줄 구분 기호를 포함할 수 없습니다.

속성 데이터에 적용되는 추가 규칙은 [텍스트 문자열](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)을 참조하십시오.
