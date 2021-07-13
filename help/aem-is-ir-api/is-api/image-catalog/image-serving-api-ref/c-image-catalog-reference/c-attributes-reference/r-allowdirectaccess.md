---
description: 경로 기반 자산에 직접 액세스할 수 있습니다.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

경로 기반 자산에 직접 액세스할 수 있습니다.

이 속성이 정의되면 `include` 또는 `exclude` 키워드를 사용하는지에 따라 지정된 개체 유형에 대해 경로 기반 액세스가 허용되거나 제한됩니다.

>[!NOTE]
>
>`AllowDirectAccess` 속성을 지정하지 않으면 기본값은 `exclude`입니다.

* `include` 지정한 개체 유형에 대한 액세스를 허용하고 다른 모든 개체 유형에 대한 액세스를 제한합니다.
* `exclude` 지정된 객체 유형에 대한 액세스를 제한하고 다른 모든 객체에 대한 액세스를 허용합니다.

`include` 및 `exclude` 가 지정되지 않은 경우 `include` 가 가정됩니다.

다음 유형을 제어할 수 있습니다.

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 예제 {#section-4c3765ebaa4245a799b454fc196f9237}

* `IS` 및 `STATIC` 개체 유형에 대해서만 직접 액세스 허용

   `AllowDirectAccess=include:IS,STATIC`

* `IS` 및 `STATIC``AllowDirectAccess=exclude:IS,STATIC` 이외의 모든 개체 유형에 대해 직접 액세스 허용

* *개체 유형 없음*&#x200B;에 직접 액세스 허용(즉, 없음 포함)

   `AllowDirectAccess=include:`

* *모든* 개체 유형에 대해 직접 액세스 허용(즉, 제외 없음)

   `AllowDirectAccess=exclude:`

* `include:IS,STATIC`에 해당합니다. `include`/ `exclude`가 없으면 `include`이 가정됩니다.

   `AllowDirectAccess=IS,STATIC`

   이 회사에 대해 `AllowDirectAccess` 속성이 지정되지 않은 경우 사용되는 기본값입니다.

* `include:`에 해당하는 없음 포함(`include`/ `exclude`이 없으면 `include`이 가정됨)

   `AllowDirectAccess=`
