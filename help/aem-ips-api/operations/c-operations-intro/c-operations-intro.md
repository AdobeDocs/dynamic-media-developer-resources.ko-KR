---
description: IPS 웹 서비스 API에서 처리하는 일반적인 작업 매개 변수에 대해 설명합니다.
solution: Experience Manager
title: 작업 메서드
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# 작업 메서드{#operations-methods}

이 섹션에서는 IPS 웹 서비스 API에서 처리하는 일반적인 작업 매개 변수에 대해 설명합니다.

각 작업 매개변수에 대한 자세한 내용은 [작업 매개 변수](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## 핸들: 정보 {#section-094ce1afa6244fa5b2c762f44ffdca1c}

특정 API 작업에서 반환된 참조 IPS 개체를 처리합니다. 핸들을 매개 변수로 후속 작업 호출에 전달할 수도 있습니다. 핸들은 문자열 데이터 유형입니다( `xsd:string`).

핸들은 단일 애플리케이션 세션 동안에만 사용됩니다. 또한 IPS 릴리스 간에 형식이 변경될 수 있으므로 핸들을 지속적으로 만들어야 합니다. 대화형 응용 프로그램을 작성할 때 세션 시간 초과를 구현하고 특히 IPS 업그레이드 후에 세션 간의 모든 핸들을 삭제합니다. 비대화형 응용 프로그램을 작성할 때는 응용 프로그램이 실행될 때마다 핸들을 검색하도록 적절한 작업을 호출합니다. 다음 Java/Axis2 코드 샘플은 부정확하고 올바른 코드 실행을 보여 줍니다.

**잘못된 핸들 코드**

이 코드 샘플은 회사 핸들에 대해 하드 코딩된 값(555)이 포함되어 있으므로 올바르지 않습니다.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**올바른 핸들 코드**

이 코드 샘플은 `getCompanyInfo` 올바른 핸들을 반환합니다. 하드 코딩된 값에 의존하지 않습니다. 이 메서드를 사용하거나 이에 해당하는 다른 IPS API를 사용하여 필요한 핸들을 반환합니다.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## 일반 핸들 유형 {#section-e683ac8283284f9688e63f51a494f7a0}

**company핸들**

대부분의 작업에서는 를 전달하여 회사 컨텍스트를 설정해야 합니다. `companyHandle` 매개 변수. 회사 핸들은 다음과 같은 특정 작업에서 반환된 포인터입니다. `getCompanyInfo`, `addCompany`, 및 `getCompanyMembership`.

**사용자 핸들**

다음 `userHandle` 매개 변수는 특정 사용자를 대상으로 하는 작업에 대한 선택적 매개 변수입니다. 기본적으로 이러한 작업은 호출 사용자(인증을 위해 자격 증명이 전달된 사용자)를 타겟팅합니다. 그러나 적절한 권한이 있는 관리자는 다른 사용자를 지정할 수 있습니다. 예를 들어 `setPassword` 작업은 일반적으로 인증된 사용자의 암호를 설정하지만 관리자는 `userHandle` 다른 사용자의 암호를 설정하는 매개 변수입니다.

회사 컨텍스트가 필요한 작업의 경우(다음을 사용) `companyHandle` 매개 변수)를 사용하면 authenticated 사용자와 target 사용자는 모두 지정된 회사의 멤버여야 합니다. 회사 컨텍스트가 필요하지 않은 작업의 경우 인증된 사용자와 대상 사용자가 모두 하나 이상의 일반 회사의 멤버여야 합니다.

다음 작업에서는 사용자 핸들을 검색할 수 있습니다.

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle 및 accessGroupHandle**

기본적으로 액세스 권한(읽기, 쓰기, 삭제)이 필요한 작업은 호출 사용자의 권한 컨텍스트에서 작동합니다. 특정 작업을 통해 `accessUserHandle` 또는 `accessGroupHandle` 매개 변수. 다음 `accessUserHandle` 관리자는 매개 변수를 사용하여 다른 사용자를 가장할 수 있습니다. 다음 `accessGroupHandle` 매개 변수를 사용하면 호출자가 특정 사용자 그룹의 컨텍스트에서 작동할 수 있습니다.

**responseFieldArray 및 excludeFieldArray**

일부 작업을 수행하면 호출자가 응답에 포함된 필드를 제한할 수 있습니다. 필드를 제한하면 요청을 처리하는 데 필요한 시간과 메모리를 줄이고 응답 데이터의 크기를 줄이는 데 도움이 됩니다. 호출자는 를 전달하여 특정 필드 목록을 요청할 수 있습니다. `responseFieldArray` 매개 변수 또는 를 통해 제외된 필드 목록이 열거되어 있음 `excludeFieldArray` 매개 변수.

모두 `responseFieldArray` 및 `excludeFieldArray` 다음으로 구분된 노드 경로를 사용하여 필드 지정 `/`. 예를 들어, `searchAssets` 각 에셋에 대한 이름, 마지막 수정 날짜 및 메타데이터만 반환합니다.

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

마찬가지로 모든 필드 반환(권한 제외):

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

노드 경로는 반환 노드 루트에 상대적입니다. 하위 요소 없이 복합 유형 필드를 지정하는 경우(예: `assetArray/items/imageInfo`)를 입력하면 모든 하위 요소가 포함됩니다. 복합 유형 필드에 하나 이상의 하위 요소를 지정하는 경우(예: `assetArray/items/imageInfo/originalPath`)를 입력하면 해당 하위 요소만 포함됩니다.

다음을 포함하지 않는 경우 `responseFieldArray` 또는 `excludeFieldArray` 요청에서 모든 필드가 반환됩니다.

**로케일**

IPS 4.0부터 IPS API는 `authHeader` locale 매개 변수. locale 매개 변수가 없으면 HTTP 헤더가 `Accept-Language` 를 사용합니다. 이 헤더도 없으면 IPS 서버에 대한 기본 로케일이 사용됩니다.

특정 작업에서는 작업 로케일 컨텍스트와 다를 수 있는 명시적 로케일 매개 변수도 사용합니다. 예를 들어 `submitJob` 다음 작업을 수행합니다. `locale` 작업 로깅 및 전자 메일 알림에 사용되는 로케일을 설정하는 매개 변수입니다.

로케일 매개 변수는 형식을 사용합니다 `<language_code>[-<country_code>]`

언어 코드가 ISO-639에서 지정한 소문자로 된 두 자리 코드이고 국가 코드(선택 사항)가 ISO-3266에서 지정한 소문자로 된 두 자리 코드인 경우 예를 들어 미국 영어의 로케일 문자열은 `en-US`.
