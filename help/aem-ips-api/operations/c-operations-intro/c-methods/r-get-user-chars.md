---
description: 특정 필드에 사용되는 문자 목록을 가져옵니다.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 12%

---

# getUserChars{#getuserchars}

특정 필드에 사용되는 문자 목록을 가져옵니다.

구문

## 승인된 사용자 유형 {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-93107d87f1b24fc8ad276dfee5e30b63}

**입력(getUserCharsParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| charField | `xsd:string` | 예 | 검색할 휴지통 상태를 결정합니다. |
| includeInactive | `xsd:boolean` | 예 | 비활성 사용자를 포함하거나 제외합니다. IPS 관리자가 아닌 사용자는 API 호출을 수행할 수 있는 권한을 부여받으려면 적어도 한 회사의 활성 멤버여야 합니다. 사용자에게 활성 회사 멤버십이 없으면 인증 오류가 반환됩니다. |
| includInvalid | `xsd:boolean` | 아니요 | 잘못된 사용자를 포함하거나 제외합니다. |
| companyHandleArray | `types:HandleArray` | 아니요 | 회사를 기준으로 결과를 필터링합니다. |
| groupHandleArray | `types:HandleArray` | 아니요 | 그룹을 기반으로 결과를 필터링합니다. |
| userRoleArray | `types:StringArray` | 아니요 | 사용자 역할을 기반으로 결과를 필터링합니다. |
| numChars | `xsd:int` | 아니요 | 1자 이상을 사용합니다. |

**출력(getUserCharsReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| userCharsArray | `types:StringArray` | 예 | 문자 접두사의 배열입니다. |

## 예제 {#section-3702f165e8b041139a6144f4a76ca25f}

이 코드 샘플은 다음을 반환합니다.

* 특정 회사 사용자의 성 첫 글자.
* 그룹 집합.
* 사용자 역할 세트입니다.

사용자 문자 필터 필드 문자열 상수는 반환되는 사용자 문자 유형을 결정합니다.

**요청**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**응답**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```
