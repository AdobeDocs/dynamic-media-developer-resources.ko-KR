---
description: 자산의 이름을 변경합니다.
seo-description: 자산의 이름을 변경합니다.
seo-title: renameAsset
solution: Experience Manager
title: renameAsset
topic: Scene7 Image Production System API
uuid: f285d7e4-00df-4d90-a05a-71747a4c54cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# renameAsset{#renameasset}

자산의 이름을 변경합니다.

>[!NOTE]
>
>이 `renameFiles` 매개 변수는 이전 릴리스에 대해 더 이상 사용되지 않으며 에서 `renameAsset`제거되었습니다. 실제 파일 경로는 영향을 받지 않지만 새 자산 이름과 일치하도록(파일 확장명 유지) 가상 파일 경로가 변경됩니다. API 클라이언트는 새 API 버전으로 업데이트할 때 이 매개 변수에 대한 참조를 제거해야 합니다.

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
| ` *`companyHandle`*` | `xsd:string` | 예 | 자산이 속하는 회사의 핸들. |
| ` *`assetHandle`*` | `xsd:string` | 예 | 이름을 변경할 자산의 핸들입니다. |
| ` *`newName`*` | `xsd:string` | 예 | 자산의 새 이름입니다. |
| ` *`validateName`*` | `xsd:boolean` | 예 | 가 `validateName` 있는 경우 자산 유형에 고유한 IPS ID가 필요한 `true` 경우 새 이름에 전역 고유성이 확인되고 고유하지 않은 경우 오류가 `renameAsset` 발생합니다. |

**출력(renameAssetReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다. 이 요소에 대한 경고가 필요하면 `<ns1:validateName>` 요소의 설명을 참조하십시오.

## 예제 {#section-a0ddffd62bec42e09069f22ceb486f8a}

이 코드 샘플은 자산의 이름을 변경합니다.

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
