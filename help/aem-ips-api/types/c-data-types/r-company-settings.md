---
description: 회사별 구성 설정.
solution: Experience Manager
title: 회사 설정
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 2%

---

# [!DNL CompanySettings]{#companysettings}

회사별 구성 설정.

구문

## 매개 변수 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 이름 | 유형 | 설명 |
|---|---|---|
| overwriteMode | `xsd:string` | 동일한 기본 이미지 이름 및 확장명으로 현재 폴더의 이미지를 덮어쓸지 여부를 결정합니다. |
| keepPublishState | `xsd:boolean` | IPS에 업로드된 대체 이미지가 기존 &quot;게시 준비&quot; 설정을 유지할지 또는 업로드에서 지정한 대로 지정할지를 지정합니다. |
| defaultSourceProfile | `types:Asset` | CMYK 이미지 파일을 추가할 때 &quot;기본 색상 동작 사용&quot;의 일부로 자동으로 적용되는 기본 소스 색상 프로파일(Coated FOGRA27(ISO 126472:2004)을 지정합니다. |
| defaultDisplayProfile | `types:Asset` | CMYK 이미지 파일을 추가할 때 &quot;기본 색상 동작 사용&quot;의 일부로 자동으로 적용되는 기본 내부 색상 프로파일(SWOP) v2)을 지정합니다. |
| iptcExifMappingXslt | `types:Asset` | IPTC 및 EXIF 이미지 헤더 데이터를 IPS로 추출하려면 내부 필드 이름에서 회사의 사용자 정의 필드 이름으로 변환해야 합니다. 업로드된 이미지에 대한 XSL 변환 테이블(기본값은 &quot;IPTC 또는 EXIF 필드를 추출하지 않음&quot;)을 결정합니다. |
| xmpMappingXslt | `types:Asset` | XMP 이미지 헤더 데이터를 IPS로 추출하려면 내부 필드 이름에서 회사의 사용자 정의 필드 이름으로 변환해야 합니다. 업로드된 이미지에 대한 XSL 변환 테이블(기본값은 &quot;XMP 필드를 추출하지 않음&quot;)을 결정합니다. |
| diskSpaceWarningMin | `xsd:int` | 경고가 전송되기 전에 이미지 디렉터리의 사용 가능한 디스크 공간이 최소 양입니다. |
| emailTrashCleanupWarning | `xsd:boolean` | 휴지통으로 가져온 항목이 자동으로 삭제되기 전에 이메일을 전송할지 여부를 결정합니다. |
| javascriptUploadEnabled | `types:Asset` | JavaScript 파일을 업로드할지 여부를 결정합니다. 이는 잠재적인 보안 위험이므로 이 옵션은 주의 깊게 사용하십시오. |
