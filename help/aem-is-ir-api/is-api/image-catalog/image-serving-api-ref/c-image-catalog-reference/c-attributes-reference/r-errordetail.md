---
description: 오류 메시지 세부 정보. HTTP를 통해 반환되는 오류 메시지에 대한 세부 수준을 error.message 값으로 지정합니다.
solution: Experience Manager
title: 오류 세부 정보
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 4%

---

# 오류 세부 정보{#errordetail}

오류 메시지 세부 정보. HTTP를 통해 반환되는 오류 메시지에 대한 세부 수준을 error.message 값으로 지정합니다.

허용되는 값은 다음과 같습니다.

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>제목만 오류에 대한 간단한 일반 설명을 반환합니다. 공개적으로 액세스할 수 있는 라이브 서버에 권장됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>간단한 메시지. 향후 사용을 위해 예약되었습니다. 현재 동일한 정보를 0으로 반환합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>자세한 메시지. 오류에 대한 사용자 수준 세부 정보를 제공합니다. 파일 경로와 같은 중요한 정보를 포함할 수 있습니다. 스테이징, 품질 보증 및 애플리케이션 개발 서버에 권장됩니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>전체 디버그 정보. 해당되는 경우 Java 스택 추적을 추가합니다. 오류 이미지에는 스택 추적이 포함되지 않고 대신 레벨 2 정보가 반환됩니다. <span class="codeph"> $error.message</span>. 이 정보는 Dynamic Media 기술 지원에 문제를 보고할 때 유용할 수 있습니다. </p></td> 
 </tr> 
</table>

## 속성 {#section-e167895723ca4ad4ba283d3d7b4324de}

열거형 값은 0, 1, 2 또는 3이어야 합니다.

## 기본값 {#section-8f27098e509945a18676aca0675c8f41}

상속 위치 `default::ErrorDetail` 지정되지 않았거나 비어 있는 경우.

## 참조 {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
