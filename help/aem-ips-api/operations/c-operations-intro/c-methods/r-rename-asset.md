---
description: 자산 이름을 변경합니다.
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 7%

---

# renameAsset{#renameasset}

자산 이름을 변경합니다.

>[!NOTE]
>
>다음 `renameFiles` 매개 변수는 이전 릴리스에서 더 이상 사용되지 않으며 다음에서 제거되었습니다. `renameAsset`. 가상 파일 경로가 새 자산 이름과 일치하도록(파일 확장명 유지) 변경되지만 실제 파일 경로는 영향을 받지 않습니다. API 클라이언트는 새 API 버전으로 업데이트할 때 이 매개 변수에 대한 참조를 제거해야 합니다.

## 인증된 사용자 유형 {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>사용자는 자산에 대한 읽기 및 쓰기 액세스 권한이 있어야 합니다.

## 매개 변수 {#section-ef95a994106841e0ab346dd4cf672258}

**입력(renameAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 예 | 자산이 속한 회사의 핸들. |
| assetHandle | `xsd:string` | 예 | 이름을 바꿀 자산의 핸들입니다. |
| newName | `xsd:string` | 예 | 자산의 새 이름입니다. |
| validateName | `xsd:boolean` | 예 | 만약 `validateName` is `true` 자산 유형에는 고유한 IPS ID가 필요한 경우 새 이름에 글로벌 고유성과 고유성이 있는지 확인합니다 `renameAsset` 고유하지 않으면 오류를 발생합니다. |

**출력(renameAssetReturn)**

IPS API가 이 작업에 대한 응답을 반환하지 않습니다. 의 설명을 참조하십시오. `<ns1:validateName>` 이 요소에 대한 경고 요소입니다.

## 예제 {#section-a0ddffd62bec42e09069f22ceb486f8a}

이 코드 샘플은 자산의 이름을

**요청**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**응답**

없음.
