---
description: 여러 텍스트와 이미지 레이어를 포함할 수 있는 레이어 이미지를 만듭니다.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
TQID: 'https://experienceleague.adobe.com/T9x2yuGOkwJ5xp6CVyREMySIy7HYL58jYI3-J2E2K6g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 9%

---

# createTemplate{#createtemplate}

여러 텍스트와 이미지 레이어를 포함할 수 있는 레이어 이미지를 만듭니다.

`urlModifier` 매개 변수는 URL에서 사용자가 제공한 명령 앞에 적용된 이미지 서버 카탈로그에 저장된 이미지 서버 프로토콜 명령을 지정합니다. `urlPostApplyModifier` 매개 변수는 충돌하는 사용자 제공 설정을 무시하는 URL 명령 뒤에 적용되는 프로토콜 명령을 지정합니다.

## 승인된 사용자 유형 {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**입력(createTemplateParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| company핸들 | `xsd:string` | 예 | 템플릿이 속한 회사입니다. |
| folder핸들 | `xsd:string` | 예 | 템플릿이 있는 폴더를 나타내는 폴더 핸들입니다. |
| name | `xsd:string` | 예 | 템플릿 이름. |
| 유형 | `xsd:string` | 예 | 템플릿 유형. |
| urlModifier | `xsd:string` | 예 | URL에서 사용자가 제공한 명령 앞에 적용되는 IS 카탈로그에 저장된 이미지 서버 명령을 지정합니다. |
| urlPostApplyModifier | `xsd:string` | 아니요 | 충돌하는 사용자 제공 설정을 무시하는 URL 명령 뒤에 적용되는 프로토콜 명령을 지정합니다. |

**출력(createTemplateParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| assetHandle | `xsd:string` | 예 | 템플릿에 대한 핸들입니다. |

## 예제 {#section-09adb4d2f0c944af875c4463a461f55d}

이 코드 샘플은 핸들로 지정된 폴더에 `APIcreateTemplate`, `urlModifier` 및 `urlPostApplyModifier` 이름의 템플릿을 만듭니다. 응답은 새로 만든 템플릿에 핸들을 반환합니다.

**요청**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**응답**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```
