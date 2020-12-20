---
description: 오류 응답 이미지. 이미지 제공에서는 일반적으로 오류가 발생할 때 텍스트 메시지와 함께 오류 상태를 반환합니다.
seo-description: 오류 응답 이미지. 이미지 제공에서는 일반적으로 오류가 발생할 때 텍스트 메시지와 함께 오류 상태를 반환합니다.
seo-title: ErrorImage
solution: Experience Manager
title: ErrorImage
topic: Scene7 Image Serving - Image Rendering API
uuid: b071c0cd-e7b8-422b-9b23-d93f504d9ce5
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 1%

---


# ErrorImage{#errorimage}

오류 응답 이미지. 이미지 제공에서는 일반적으로 오류가 발생할 때 텍스트 메시지와 함께 오류 상태를 반환합니다.

`attribute::ErrorImage` 오류 발생 시 이미지, 카탈로그 항목 또는 템플릿을 표시하도록 허용합니다.

>[!NOTE]
>
>누락된 이미지는 `attribute::DefaultImage`으로 처리할 수도 있습니다.

오류 메시지 텍스트를 응답 이미지로 렌더링할 수 있는 이미지 제공 템플릿을 구성할 수 있습니다. 다음 사전 정의된 변수를 `$error.title` 템플릿에 포함할 수 있습니다. 이 변수는 짧은 오류 설명으로 대체되며, 보다 자세한 오류 설명(세부 수준 `attribute::ErrorDetail`으로 구성)으로 대체됩니다.`$error.message`

오류 이미지/템플릿을 처리할 수 있는 경우 HTTP 상태 200이 반환됩니다. 이 처리 중에 오류가 발생하면 HTTP 오류 상태 및 텍스트 메시지가 반환됩니다.

## 속성 {#section-f460c6c2dd1f46b29f9a79b093575f45}

텍스트 문자열. 지정된 경우 이미지 카탈로그의 유효한 카탈로그::Id 값 또는 이미지 서버에서 액세스할 수 있는 이미지 파일의 상대(a0/>에 대한) 또는 절대 경로여야 합니다.`attribute::RootPath`

## 기본값 {#section-2885f289e5714ddca665a6aee401967f}

정의되지 않은 경우 `default::ErrorImage`에서 상속됩니다. 정의되지만 비어 있으면 `default::ErrorImage`이(가) 정의되어 있고 HTTP 오류 상태 및 텍스트 메시지가 반환되더라도 오류 이미지 동작이 비활성화됩니다.

## 예 {#section-c92090abe1d247529542a8dd4960c2e6}

이미지에 렌더링되는 오류 메시지와 함께 응답 이미지를 가져오려면 먼저 이미지 카탈로그에서 템플릿을 정의해야 합니다. 이 경우 `catalog::Modifier`에 다음 내용이 포함된 `onError`이라는 이미지 카탈로그에 항목을 만듭니다.

`size=300,300&bgc=ffffff&text=$error.message$`

템플릿이 `attribute::ErrorImage`에 등록되었습니다.

`ErrorImage=myCatalog/onError`

이 예에서 텍스트는 기본 글꼴, 글꼴 색상 및 글꼴 크기를 사용하여 렌더링됩니다.

## 참조 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[속성::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ,  [카탈로그::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [속성::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [속성::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
