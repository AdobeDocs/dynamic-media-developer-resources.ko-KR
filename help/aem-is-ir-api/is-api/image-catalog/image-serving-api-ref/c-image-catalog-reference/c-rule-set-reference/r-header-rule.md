---
description: HTTP 응답 헤더 요소입니다. 선택 사항입니다 <rule> 요소를 생성하지 않습니다.
solution: Experience Manager
title: 헤더
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# 헤더{#header}

HTTP 응답 헤더 요소입니다. 선택 사항입니다 `<rule>` 요소를 생성하지 않습니다.

## 속성 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*텍스트*&quot;** : 필수 여부. HTTP 헤더의 이름을 지정합니다.

**`Action`= &quot;set&quot; |`"add"`**: 선택 사항입니다. 기본값은 입니다. `"set"`: 현재 헤더 값을 대체합니다. 지정 `"add"` 을 입력하여 헤더 값을 쉼표로 구분하여 추가합니다.

## 데이터 {#section-a387f541396c49d99c29692a38032914}

헤더 값.

## 설명 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

사전 정의된 헤더의 값을 추가하거나 바꿀 수 있을 뿐만 아니라 새 HTTP 응답 헤더를 추가할 수 있습니다. 이름 및 값은 HTTP 표준을 준수해야 합니다. 추가 인코딩은 적용되지 않습니다.

이미지 제공 대체 변수는 헤더 이름 및 헤더 값에 사용할 수 있습니다. 이렇게 하면 요청에서 두 문자열을 제어할 수 있습니다.

## 예 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

다음 규칙은 요청에 헤더 값이 변수로 지정된 경우 사용자 지정 헤더를 적용합니다.

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

이 규칙은 HTTP 응답 헤더를 설정하는 다음 요청에 의해 트리거됩니다 `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
