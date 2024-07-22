---
description: 에셋의 이름을 바꿉니다.
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 6%

---

# renameAsset{#renameasset}

에셋의 이름을 바꿉니다.

>[!NOTE]
>
>`renameFiles` 매개 변수는 이전 릴리스에서 더 이상 사용되지 않으며 `renameAsset`에서 제거되었습니다. 가상 파일 경로는 새 자산 이름과 일치하도록 변경되지만(파일 확장명 유지) 실제 파일 경로는 영향을 받지 않습니다. API 클라이언트는 새 API 버전으로 업데이트할 때 이 매개 변수에 대한 참조를 제거해야 합니다.

## 승인된 사용자 유형 {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>사용자에게 에셋에 대한 읽기 및 쓰기 권한이 있어야 합니다.

## 매개 변수 {#section-ef95a994106841e0ab346dd4cf672258}

**입력(renameAssetParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 자산이 속한 회사에 대한 핸들입니다. |
| assetHandle | `xsd:string` | 예 | 이름을 바꿀 에셋에 대한 핸들입니다. |
| newName | `xsd:string` | 예 | 에셋의 새 이름입니다. |
| validateName | `xsd:boolean` | 예 | `validateName`이(가) `true`이고 에셋 유형에 고유한 IPS ID가 필요한 경우 새 이름에 전역 고유성이 확인되며 `renameAsset`에서 고유하지 않은 경우 오류가 발생합니다. |

**출력(renameAssetReturn)**

IPS API는 이 작업에 대한 응답을 반환하지 않습니다. 이 요소에 대한 주의 사항은 `<ns1:validateName>` 요소에 대한 설명을 참조하십시오.

## 예제 {#section-a0ddffd62bec42e09069f22ceb486f8a}

이 코드 샘플은 에셋 이름을 바꿉니다.

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
