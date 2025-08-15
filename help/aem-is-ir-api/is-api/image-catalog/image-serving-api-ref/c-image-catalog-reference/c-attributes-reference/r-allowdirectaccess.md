---
description: 경로 기반 자산에 직접 액세스할 수 있습니다.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

경로 기반 자산에 직접 액세스할 수 있습니다.

이 특성이 정의된 경우 `include` 또는 `exclude` 키워드를 사용하는지 여부에 따라 지정된 개체 형식에 대해 경로 기반 액세스가 허용되거나 제한됩니다.

>[!NOTE]
>
>`AllowDirectAccess` 특성이 지정되지 않은 경우 기본값은 `exclude`입니다.

* `include`은(는) 지정한 개체 형식에 대한 액세스를 허용하고 다른 모든 개체에 대한 액세스를 제한합니다.
* `exclude`은(는) 지정한 개체 형식에 대한 액세스를 제한하고 다른 모든 개체에 대한 액세스를 허용합니다.

`include`과(와) `exclude`을(를) 모두 지정하지 않으면 `include`이(가) 간주됩니다.

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

* `IS` 및 `STATIC` `AllowDirectAccess=exclude:IS,STATIC`을(를) 제외한 모든 개체 유형에 대해 직접 액세스 허용

* *no* 개체 형식에 대한 직접 액세스 허용(즉, 포함하지 않음)

  `AllowDirectAccess=include:`

* *모든* 개체 유형에 대한 직접 액세스 허용(즉, 제외 없음)

  `AllowDirectAccess=exclude:`

* `include:IS,STATIC`과(와) 동일합니다(`include`/ `exclude`이(가) 없는 경우 `include`으로 가정).

  `AllowDirectAccess=IS,STATIC`

  이 회사에 대해 `AllowDirectAccess` 특성이 지정되지 않은 경우 사용되는 기본값입니다.

* `include:`과(와) 동등한 `include`/ `exclude`이(가) 없으면 `include`으로 간주됩니다.

  `AllowDirectAccess=`
