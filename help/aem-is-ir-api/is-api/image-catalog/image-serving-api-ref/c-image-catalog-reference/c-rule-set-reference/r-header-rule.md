---
description: HTTP 응답 헤더 요소입니다. 에서 선택 사항 <rule> 요소.
solution: Experience Manager
title: 헤더
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# 헤더{#header}

HTTP 응답 헤더 요소입니다. 에서 선택 사항 `<rule>` 요소.

## 속성 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*텍스트*&quot;** : 필수. HTTP 헤더의 이름을 지정합니다.

**`Action`= &quot;set&quot; |`"add"`**: 선택 사항입니다. 기본값은 입니다 `"set"`: 현재 헤더 값을 대체합니다. 지정 `"add"` 헤더 값을 추가합니다. 쉼표로 구분합니다.

## 데이터 {#section-a387f541396c49d99c29692a38032914}

헤더 값.

## 설명 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

새 HTTP 응답 헤더를 추가하고 사전 정의된 헤더 값을 추가하거나 바꿀 수 있습니다. 이름과 값은 HTTP 표준을 준수해야 합니다. 추가 인코딩이 적용되지 않습니다.

헤더 이름 및 헤더 값에는 이미지 제공 대체 변수가 사용될 수 있습니다. 이를 통해 요청에서 두 문자열을 제어할 수 있습니다.

## 예 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

다음 규칙은 헤더 값이 요청에 변수로 지정된 경우 사용자 지정 헤더를 적용합니다.

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

이 규칙은 HTTP 응답 헤더를 설정하는 다음 요청에 의해 트리거됩니다. `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
