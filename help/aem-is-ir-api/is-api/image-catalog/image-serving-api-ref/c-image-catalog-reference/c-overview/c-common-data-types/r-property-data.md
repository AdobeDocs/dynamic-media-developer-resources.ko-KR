---
description: 속성 데이터는 하나 이상의 속성을 나타내는 텍스트 문자열로 구성됩니다.
solution: Experience Manager
title: 속성 데이터
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86278720-ece0-4e67-8fb1-443355f878b7
TQID: 'https://experienceleague.adobe.com/jE8U1fgDsG9wdzG4O-BsPHvPOGLXDxZRMdZvL9LuYZE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 110
ht-degree: 0%

---

# 속성 데이터{#property-data}

속성 데이터는 하나 이상의 속성을 나타내는 텍스트 문자열로 구성됩니다.

속성은 속성 이름과 속성 값으로 구성되며, =로 구분됩니다.

여러 속성은 줄 구분 기호로 구분되며, 줄 구분 기호는 `??` 또는 `<CR><LF>`일 수 있습니다. 전체 속성 데이터 문자열이 따옴표로 묶여 있지 않으면 서버에서 각 `??` 항목을 `<CR><LF>`(으)로 바꾼 후 데이터를 클라이언트에 전송합니다. 속성 이름은 문자, 숫자, &#39;.&#39;, &#39;-&#39; 및 &#39;_&#39;로 구성될 수 있습니다. 속성 이름은 대/소문자를 구분하지 않습니다.

속성 값에는 줄 구분 기호를 포함하지 않아야 합니다.

속성 데이터에 적용되는 추가 규칙은 [텍스트 문자열](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63)을(를) 참조하십시오.
