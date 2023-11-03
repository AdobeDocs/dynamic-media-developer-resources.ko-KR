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

이 속성을 정의하면 지정된 객체 유형에 대해 경로 기반 액세스가 허용되거나 제한됩니다. `include` 또는 `exclude` 키워드가 사용됩니다.

>[!NOTE]
>
>다음과 같은 경우 `AllowDirectAccess` 속성이 지정되지 않았습니다. 기본값은 입니다. `exclude`.

* `include` 지정된 객체 유형에 대한 액세스를 허용하고 다른 모든 유형에 대한 액세스를 제한합니다.
* `exclude` 지정된 객체 유형에 대한 액세스를 제한하고 다른 모든 유형에 대한 액세스를 허용합니다.

둘 다 아닌 경우 `include` nor `exclude` 을(를) 지정했습니다. `include` 가 가정됩니다.

다음 유형을 제어할 수 있습니다.

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 예제 {#section-4c3765ebaa4245a799b454fc196f9237}

* 다음에 대한 직접 액세스만 허용 `IS` 및 `STATIC` 오브젝트 유형

  `AllowDirectAccess=include:IS,STATIC`

* 다음을 제외한 모든 오브젝트 유형에 대해 직접 액세스 허용 `IS` 및 `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* 다음에 대한 직접 액세스 허용 *아니요* 객체 유형(즉, 포함하지 않음)

  `AllowDirectAccess=include:`

* 다음에 대한 직접 액세스 허용 *모두* 객체 유형(즉, 제외 없음)

  `AllowDirectAccess=exclude:`

* 등가물 `include:IS,STATIC` (if `include`/ `exclude` 이(가) 없음, `include` 가정)

  `AllowDirectAccess=IS,STATIC`

  는 다음과 같은 경우에 사용되는 기본값입니다. `AllowDirectAccess` 이 회사에 대한 특성이 지정되지 않았습니다.

* 포함하지 않음, 해당 항목 `include:` (if `include`/ `exclude` 이(가) 없음, `include` 가정)

  `AllowDirectAccess=`
