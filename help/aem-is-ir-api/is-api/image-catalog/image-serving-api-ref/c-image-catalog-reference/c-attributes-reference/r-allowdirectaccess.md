---
description: 경로 기반 자산에 직접 액세스 허용
seo-description: 경로 기반 자산에 직접 액세스 허용
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AllowDirectAccess{#allowdirectaccess}

경로 기반 자산에 직접 액세스 허용

이 속성이 정의되면 지정된 객체 유형에 대해 `include` 또는 `exclude` 키워드의 사용 여부에 따라 경로 기반 액세스가 허용되거나 제한됩니다.

>[!NOTE]
>
>속성이 지정되지 않은 `AllowDirectAccess` 경우 기본값은 `exclude`입니다.

* `include` 지정된 객체 유형에 대한 액세스를 허용하고 다른 모든 객체에 대한 액세스를 제한합니다.
* `exclude` 지정된 객체 유형에 대한 액세스를 제한하고 다른 모든 객체에 대한 액세스를 허용합니다.

지정하지 `include` 않거나 `exclude` 지정하지 않으면 `include` 으로 간주됩니다.

다음 유형을 제어할 수 있습니다.

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 예제 {#section-4c3765ebaa4245a799b454fc196f9237}

* 객체 `IS` 및 `STATIC` 객체 유형에 대해서만 직접 액세스 허용

   `AllowDirectAccess=include:IS,STATIC`

* 및 `IS``STATIC``AllowDirectAccess=exclude:IS,STATIC`

* 객체 유형이 *없는* 경우(예: 없음 포함) 직접 액세스 허용

   `AllowDirectAccess=include:`

* 모든 ** 객체 유형에 직접 액세스 허용(예: 제외 없음)

   `AllowDirectAccess=exclude:`

* 에 `include:IS,STATIC` ( `include`/ `exclude` 가 없는 경우 `include` 가정됨)에 해당합니다.

   `AllowDirectAccess=IS,STATIC`

   이 회사에 대한 속성이 지정되지 않은 경우 사용되는 `AllowDirectAccess` 기본값입니다.

* none을 포함하되 이에 준하는 `include:` 경우 `include`/가 `exclude` 없는 경우 `include` 간주합니다.

   `AllowDirectAccess=`

