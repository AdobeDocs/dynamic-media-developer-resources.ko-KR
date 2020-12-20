---
description: HTTP 응답 헤더 요소입니다. <rule> 요소의 선택 사항입니다.
seo-description: HTTP 응답 헤더 요소입니다. <rule> 요소의 선택 사항입니다.
seo-title: 헤더
solution: Experience Manager
title: 헤더
topic: Scene7 Image Serving - Image Rendering API
uuid: 89ec0f27-fc12-47c2-b9dd-e0ee768587b5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---


# 헤더{#header}

HTTP 응답 헤더 요소입니다. `<rule>` 요소의 선택 사항입니다.

## 속성 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** :필수. HTTP 헤더의 이름을 지정합니다.

**`Action`= &quot;set&quot; |`"add"`**:선택 사항. 기본값은 현재 헤더 값을 대체하는 `"set"`입니다. `"add"`을 지정하여 머리글 값을 쉼표로 구분하여 추가합니다.

## 데이터 {#section-a387f541396c49d99c29692a38032914}

헤더 값.

## 설명 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

사전 정의된 헤더의 값을 추가하거나 바꾸는 것은 물론 새 HTTP 응답 헤더를 추가할 수 있습니다. 이름과 값은 HTTP 표준을 준수해야 합니다. 추가 인코딩은 적용되지 않습니다.

이미지 제공 대체 변수는 헤더 이름 및 헤더 값에 사용할 수 있습니다. 이렇게 하면 요청에서 두 문자열을 모두 제어할 수 있습니다.

## 예 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

다음 규칙은 요청에 변수로 헤더 값을 지정할 때 사용자 지정 헤더를 적용합니다.

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

이 규칙은 HTTP 응답 헤더 `Edge-Control::no-store`을(를) 설정하여 다음 요청에 의해 트리거됩니다.

`http://server/is/image/cat/id?$Edge-Control=no-store`
