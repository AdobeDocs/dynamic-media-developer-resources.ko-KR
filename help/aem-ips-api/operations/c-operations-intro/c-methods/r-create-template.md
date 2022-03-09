---
description: 여러 텍스트 및 이미지 레이어가 있는 레이어 이미지를 만듭니다.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 10%

---

# createTemplate{#createtemplate}

여러 텍스트 및 이미지 레이어가 있는 레이어 이미지를 만듭니다.

다음 `urlModifier` 매개 변수는 URL에서 사용자가 제공한 명령 전에 적용된 이미지 서버 카탈로그에 저장된 이미지 서버 프로토콜 명령을 지정합니다. 다음 `urlPostApplyModifier` 매개 변수는 URL 명령 다음에 적용되는 프로토콜 명령을 지정하며, 이 명령은 충돌하는 사용자 제공 설정을 덮어씁니다.

## 인증된 사용자 유형 {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**입력(createTemplateParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| companyHandle | `xsd:string` | 예 | 템플릿이 속한 회사입니다. |
| folderHandle | `xsd:string` | 예 | 템플릿이 있는 폴더를 나타내는 폴더 핸들입니다. |
| 이름 | `xsd:string` | 예 | 템플릿 이름. |
| 유형 | `xsd:string` | 예 | 템플릿 유형. |
| urlModifier | `xsd:string` | 예 | URL에서 사용자가 제공한 명령 전에 적용되는 IS 카탈로그에 저장된 이미지 서버 명령을 지정합니다. |
| urlPostApplyModifier | `xsd:string` | 아니요 | 충돌하는 사용자 제공 설정을 재정의하는 URL 명령 다음에 적용되는 프로토콜 명령을 지정합니다. |

**출력(createTemplateParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| assetHandle | `xsd:string` | 예 | 템플릿의 핸들입니다. |

## 예제 {#section-09adb4d2f0c944af875c4463a461f55d}

이 코드 샘플은 핸들이 지정한 폴더에 이름이 `APIcreateTemplate`, `urlModifier`, 및 `urlPostApplyModifier`. 응답은 핸들을 새로 만든 템플릿에 반환합니다.

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
