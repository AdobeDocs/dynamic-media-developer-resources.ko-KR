---
title: 오류 세부 정보
description: 오류 메시지 세부 정보. HTTP를 통해 반환되는 오류 메시지의 상세 수준을 error.message 값으로 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 4%

---

# 오류 세부 정보{#errordetail}

오류 메시지 세부 정보. HTTP를 통해 반환되는 오류 메시지의 상세 수준을 error.message 값으로 지정합니다.

## 제목 {#section-c10d75d72ee24d16a67cc8d927f1deba}

허용되는 값은 다음과 같습니다.

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>제목만 오류에 대한 간단한 일반 설명을 반환합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>간단한 메시지. 향후 사용을 위해 예약되었습니다. 현재 동일한 정보를 0으로 반환합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>자세한 메시지. 오류에 대한 사용자 수준 세부 정보를 제공합니다. 파일 경로와 같은 중요한 정보를 포함할 수 있습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>전체 디버그 정보. 해당되는 경우 Java™ 스택 추적을 추가합니다. 오류 이미지에는 스택 추적이 포함되지 않고 대신 <span class="codeph"> $error.message</span>에 수준 2 정보를 반환합니다. </p></td> 
 </tr> 
</table>

* 공개적으로 액세스할 수 있는 라이브 서버에는 레벨 0이 권장됩니다.
* 스테이징, 품질 보증 및 애플리케이션 개발 서버에는 레벨 2가 권장됩니다.
* 레벨 3 정보는 Dynamic Media 기술 지원에 문제를 보고할 때 유용할 수 있습니다.

## 속성 {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

열거형 값은 0, 1, 2 또는 3이어야 합니다.

## 기본값 {#section-5e78d550050840cc9a1de811c581b94f}

지정하지 않았거나 비어 있는 경우 `default::ErrorDetail`에서 상속됩니다.

## 참조 {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
