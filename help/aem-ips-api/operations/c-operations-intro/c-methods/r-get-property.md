---
description: 이미지 포털과 관련된 시스템 속성의 문자열 값을 가져옵니다.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 12%

---

# getProperty{#getproperty}

이미지 포털과 관련된 시스템 속성의 문자열 값을 가져옵니다.

지원되는 시스템 속성은 다음과 같습니다.

* `IpsVersion`: IPS 버전 번호
* `IpsImageServerUrl`: IPS 이미지 서버의 전체 외부 URL 접두사
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: SVG 자산 렌더링용 URL 접두사입니다.
* `SvgRenderEnabled`: SVG 자산을 `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`: 업로드에 허용되는 파일 데이터의 최대 크기(바이트)입니다 [!DNL POST]. 시스템은 최대 제한보다 큰 파일을 거부합니다.

## 인증된 사용자 유형 {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 매개 변수 {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**입력(getPropertyParam)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 이름 | `xsd:string` | 예 | 가져올 속성의 이름입니다. |

**출력(getPropertyReturn)**

| 이름 | 유형 | 필수 | 설명 |
|---|---|---|---|
| 값 | `xsd:string` | 예 | 속성 값입니다. |

## 예제 {#section-3f80a78dd60c404181b34d3a912d7a36}

이 코드 샘플은 IPS 속성 문자열 상수를 사용하여 특정 값을 반환합니다. 이 예에서 IPS 속성은 IPS 서버의 버전입니다.

**요청**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**응답**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```
