---
description: 이 섹션에서는 IPS 웹 서비스 API에서 처리하는 일반적인 작업 매개 변수에 대해 설명합니다.
seo-description: 이 섹션에서는 IPS 웹 서비스 API에서 처리하는 일반적인 작업 매개 변수에 대해 설명합니다.
seo-title: 작업 방법
solution: Experience Manager
title: 작업 방법
topic: Scene7 Image Production System API
uuid: 713646a7-1108-4f93-bec2-3fbe7e548515
translation-type: tm+mt
source-git-commit: 806e7e670ee98e1fb6adf52ffc95fb989fa69400

---


# 작업 방법{#operations-methods}

이 섹션에서는 IPS 웹 서비스 API에서 처리하는 일반적인 작업 매개 변수에 대해 설명합니다.

각 작업 매개 변수에 대한 전체 설명은 작업 매개 [변수를](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)참조하십시오.

## 핸들:정보 {#section-094ce1afa6244fa5b2c762f44ffdca1c}

특정 API 작업에서 반환되는 참조 IPS 개체를 처리합니다. 후속 작업 호출에 대한 매개 변수로 핸들을 전달할 수도 있습니다. 핸들은 문자열 데이터 유형( `xsd:string`)입니다.

핸들은 단일 응용 프로그램 세션 동안에만 사용할 수 있습니다. 또한 IPS 릴리스 간에 해당 형식이 변경될 수 있으므로 핸들의 지속성을 유지해야 합니다. 인터랙티브한 애플리케이션을 작성할 때 세션 시간 초과를 구현하고 특히 IPS 업그레이드 후 세션 간 모든 핸들을 폐기합니다. 비대화형 응용 프로그램을 작성할 때는 응용 프로그램이 실행될 때마다 적절한 작업을 호출하여 핸들을 검색합니다. 다음 Java/Axis2 코드 샘플에서는 잘못된 코드 실행을 보여 줍니다.

**잘못된 핸들 코드**

이 코드 샘플에는 회사 핸들에 대한 하드 코딩된 값(555)이 포함되어 있으므로 잘못되었습니다.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**올바른 핸들 코드**

이 코드 샘플은 올바른 핸들을 반환하기 `getCompanyInfo` 위해 호출되므로 맞습니다. 하드 코딩된 값은 사용하지 않습니다. 이 방법 또는 기타 IPS API를 사용하여 필요한 핸들을 반환합니다.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## 일반 핸들 유형 {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

대부분의 작업을 수행하려면 `companyHandle` 매개 변수를 전달하여 회사 컨텍스트를 설정해야 합니다. 회사 핸들은 `getCompanyInfo`, `addCompany`및 `getCompanyMembership`같은 특정 작업에서 반환되는 포인터입니다.

**userHandle**

이 `userHandle` 매개 변수는 특정 사용자를 대상으로 하는 작업에 대한 선택적 매개 변수입니다. 기본적으로 이러한 작업은 호출 사용자(인증을 위해 인증서를 전달받은 사용자)를 대상으로 합니다. 그러나 적절한 권한을 가진 관리자 사용자는 다른 사용자를 지정할 수 있습니다. 예를 들어, `setPassword` 작업은 일반적으로 인증된 사용자의 암호를 설정하지만 관리자는 `userHandle` 매개 변수를 사용하여 다른 사용자의 암호를 설정할 수 있습니다.

회사 컨텍스트(매개 변수 사용)가 필요한 작업의 경우 인증된 사용자와 대상 사용자 모두 지정된 회사의 구성원이어야 합니다. `companyHandle` 회사 컨텍스트가 필요하지 않은 작업의 경우 인증된 사용자와 대상 사용자는 둘 다 적어도 하나의 공통 회사의 구성원이어야 합니다.

다음 작업은 사용자 핸들을 검색할 수 있습니다.

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle 및 accessGroupHandle**

기본적으로 액세스 권한(읽기, 쓰기, 삭제)이 필요한 작업은 호출 사용자의 권한 컨텍스트에서 작동합니다. 특정 작업을 사용하면 `accessUserHandle` 또는 `accessGroupHandle` 매개 변수를 사용하여 이 컨텍스트를 수정할 수 있습니다. 이 `accessUserHandle` 매개 변수를 사용하면 관리자가 다른 사용자를 가장할 수 있습니다. 이 `accessGroupHandle` 매개 변수를 사용하면 호출자가 특정 사용자 그룹의 컨텍스트에서 작동할 수 있습니다.

**responseFieldArray 및 excludeFieldArray**

일부 작업을 통해 호출자는 응답에 포함할 필드를 제한할 수 있습니다. 필드를 제한하면 요청을 처리하는 데 필요한 시간과 메모리를 줄이고 응답 데이터의 크기를 줄이는 데 도움이 됩니다. 호출자는 `responseFieldArray` 매개 변수를 전달하거나 매개 변수를 통해 제외된 필드 목록을 열거하여 특정 필드 목록을 요청할 수 `excludeFieldArray` 있습니다.

으로 구분된 노드 경로를 사용하여 `responseFieldArray` 필드를 지정하고 `excludeFieldArray` 필드를 지정합니다 `/`. 예를 들어 각 자산에 대한 이름, 마지막 수정 날짜 및 메타데이터만 반환하도록 지정하려면 다음을 참조하십시오. `searchAssets`

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

마찬가지로 모든 필드를 반환하려면(권한 제외):

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

노드 경로는 반환 노드 루트에 상대적입니다. 하위 요소(예: `assetArray/items/imageInfo`)가 없는 복잡한 유형 필드를 지정하면 모든 하위 요소가 포함됩니다. 복잡한 유형 필드(예: `assetArray/items/imageInfo/originalPath`)에 하위 요소를 하나 이상 지정하면 해당 하위 요소만 포함됩니다.

요청에 포함하지 `responseFieldArray` 않거나 `excludeFieldArray` 포함하지 않는 경우 모든 필드가 반환됩니다.

**로케일**

IPS 4.0 이후 IPS API는 `authHeader` locale 매개 변수를 전달하여 작업의 로케일 컨텍스트 설정을 지원합니다. locale 매개 변수가 없으면 HTTP 헤더가 `Accept-Language` 사용됩니다. 이 헤더가 없는 경우 IPS 서버의 기본 로케일이 사용됩니다.

특정 작업은 작업 로케일 컨텍스트와 다를 수 있는 명시적인 로케일 매개 변수를 사용합니다. 예를 들어, `submitJob` 작업은 작업 로깅 및 이메일 알림에 사용되는 로케일을 설정하는 `locale` 매개 변수를 사용합니다.

로케일 매개 변수는 `<language_code>[-<country_code>]`

언어 코드가 ISO-639에 의해 지정된 소문자, 두 문자 코드이고 옵션 국가 코드는 ISO-3266에 의해 지정된 대문자, 두 문자 코드입니다. 예를 들어 미국 영어의 로케일 문자열은 `en-US`입니다.
