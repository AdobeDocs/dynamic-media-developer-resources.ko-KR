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
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

경로 기반 자산에 직접 액세스 허용

이 속성을 정의하면 `include` 또는 `exclude` 키워드의 사용 여부에 따라 지정된 객체 유형에 대해 경로 기반 액세스가 허용되거나 제한됩니다.

>[!NOTE]
>
>`AllowDirectAccess` 특성이 지정되지 않은 경우 기본값은 `exclude`입니다.

* `include` 지정된 객체 유형에 대한 액세스를 허용하고 다른 모든 객체에 대한 액세스를 제한합니다.
* `exclude` 지정된 객체 유형에 대한 액세스를 제한하고 다른 모든 객체에 대한 액세스를 허용합니다.

`include` 또는 `exclude`이 지정되지 않은 경우 `include`로 가정합니다.

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

* `IS` 및 `STATIC``AllowDirectAccess=exclude:IS,STATIC`을 제외한 모든 개체 유형에 직접 액세스 허용

* *개체 유형 없음(예: 없음 포함)에 직접 액세스 허용*

   `AllowDirectAccess=include:`

* *모든* 개체 유형에 직접 액세스 허용(예: 제외 없음)

   `AllowDirectAccess=exclude:`

* `include:IS,STATIC`에 해당합니다. `include`/ `exclude`이(가) 없는 경우 `include`이(가) 가정됩니다.

   `AllowDirectAccess=IS,STATIC`

   이 회사에 대해 `AllowDirectAccess` 속성이 지정되지 않은 경우 사용되는 기본값입니다.

* 없음, `include:`에 해당하는 값 포함(`include`/ `exclude`이(가) 없는 경우 `include`은(는) 가정함)

   `AllowDirectAccess=`

