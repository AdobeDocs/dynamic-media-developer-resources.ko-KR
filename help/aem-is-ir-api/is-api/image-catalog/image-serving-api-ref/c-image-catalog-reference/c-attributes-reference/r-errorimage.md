---
description: 오류 응답 이미지입니다. 이미지 제공은 일반적으로 오류가 발생하면 텍스트 메시지와 함께 오류 상태를 반환합니다.
solution: Experience Manager
title: 오류 이미지
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---

# 오류 이미지{#errorimage}

오류 응답 이미지입니다. 이미지 제공은 일반적으로 오류가 발생하면 텍스트 메시지와 함께 오류 상태를 반환합니다.

오류 발생 시 이미지, 카탈로그 항목 또는 템플릿을 구성할 수 있도록 `attribute::ErrorImage`을(를) 허용합니다.

>[!NOTE]
>
>`attribute::DefaultImage`에서 누락된 이미지를 처리할 수도 있습니다.

오류 메시지 텍스트를 응답 이미지로 렌더링할 수 있는 이미지 제공 템플릿을 구성할 수 있습니다. 미리 정의된 다음 변수는 `$error.title` 템플릿에 포함될 수 있으며, 이 템플릿은 간단한 오류 설명으로 대체되고, `$error.message`은(는) 더 자세한 오류 설명으로 대체됩니다(`attribute::ErrorDetail`(으)로 세부 수준이 구성됨).

오류 이미지/템플릿을 성공적으로 처리할 수 있으면 HTTP 상태 200이 반환됩니다. 이 처리 중에 오류가 발생하면 HTTP 오류 상태와 텍스트 메시지가 반환됩니다.

## 속성 {#section-f460c6c2dd1f46b29f9a79b093575f45}

텍스트 문자열입니다. 지정하면 이미지 카탈로그의 유효한 catalog::Id 값이거나, 이미지 서버에서 액세스할 수 있는 이미지 파일의 상대 경로이거나(`attribute::RootPath`에 대한) 절대 경로여야 합니다.

## 기본값 {#section-2885f289e5714ddca665a6aee401967f}

정의되지 않은 경우 `default::ErrorImage`에서 상속됩니다. 정의되어 있지만 비어 있는 경우, `default::ErrorImage`이(가) 정의되어 있어도 오류 이미지 동작이 비활성화되고 HTTP 오류 상태와 텍스트 메시지가 반환됩니다.

## 예 {#section-c92090abe1d247529542a8dd4960c2e6}

이미지에 렌더링된 오류 메시지와 함께 응답 이미지를 가져오려면 먼저 이미지 카탈로그에서 템플릿을 정의해야 합니다. 이 경우 이미지 카탈로그에 `onError`(이)라는 항목을 만듭니다. 이 항목에는 `catalog::Modifier`의 다음 항목이 포함됩니다.

`size=300,300&bgc=ffffff&text=$error.message$`

템플릿이 `attribute::ErrorImage`에 등록되었습니다.

`ErrorImage=myCatalog/onError`

이 예제에서 텍스트는 기본 글꼴, 글꼴 색상 및 글꼴 크기를 사용하여 렌더링됩니다.

## 참조 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[특성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [카탈로그::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [특성::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [특성::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
