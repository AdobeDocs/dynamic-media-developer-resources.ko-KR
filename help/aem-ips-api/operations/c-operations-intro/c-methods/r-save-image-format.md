---
description: 이미지 형식을 만듭니다.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 10%

---

# saveImageFormat{#saveimageformat}

이미지 형식을 만듭니다.

>[!NOTE]
>
>`urlModifier` 필드 값은 올바른 XML로 구성되어야 합니다. 예를 들어 `&`을(를) `&`(으)로 변경합니다. IPS 사용자 인터페이스에서 `urlModfier` 값을 가져옵니다.

## 승인된 사용자 유형 {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 매개 변수 {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**입력(saveImageFormatParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 작업할 이미지 형식의 회사에 대한 핸들입니다. |
| imageFormatHandle | `xsd:string` | 아니요 | 저장할 이미지 형식 핸들입니다. |
| name | `xsd:string` | 예 | 이미지 형식 이름입니다. |
| urlModifier | `xsd:string` | 예 | 모든 IPS 프로토콜 쿼리 문자열일 수 있습니다. URL 수정자를 생성하는 가장 쉬운 방법은 IPS 사용자 인터페이스를 사용하여 수정자를 만든 다음 쿼리 문자열을 잘라내어 붙여넣는 것입니다. |

**출력(saveImageFormatReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | 예 | 이미지 형식을 처리합니다. |

## 예제 {#section-c7bd733212ef494297a97093f3af193f}

이 코드 샘플은 이미지 형식을 만듭니다. 이 예에서 `urlModifier`은(는) 올바른 HTML 형식의 IPS 사용자 인터페이스에서 해당 값으로 결정되었습니다.

**요청**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**응답**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```
