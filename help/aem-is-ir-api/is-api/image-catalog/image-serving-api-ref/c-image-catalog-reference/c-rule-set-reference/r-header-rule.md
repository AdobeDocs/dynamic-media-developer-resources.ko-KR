---
title: 헤더
description: HTTP 응답 헤더 요소입니다. <rule> 요소에서 선택 사항입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
TQID: 'https://experienceleague.adobe.com/-hGRn7zVjm8eavZIwBoiAuCqoSNYIFSSlQaSP6wuHXs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 2%

---

# 헤더{#header}

HTTP 응답 헤더 요소입니다. `<rule>` 요소에서 선택 사항입니다.

## 속성 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : 필수 필드입니다. HTTP 헤더의 이름을 지정합니다.

**`Action`= &quot;set&quot; |`"add"`**: 선택 사항입니다. 기본값은 `"set"`이며, 이 값은 현재 헤더 값을 대체합니다. 헤더 값을 쉼표로 구분하여 추가할 수 있도록 `"add"`을(를) 지정하십시오.

## 데이터 {#section-a387f541396c49d99c29692a38032914}

헤더 값.

## 설명 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

새 HTTP 응답 헤더를 추가하고 사전 정의된 헤더의 값을 추가하거나 바꿀 수 있습니다. 이름과 값은 HTTP 표준을 준수해야 합니다. 추가 인코딩이 적용되지 않습니다.

헤더 이름 및 헤더 값에는 이미지 제공 대체 변수가 사용될 수 있습니다. 이를 통해 요청에서 두 문자열을 제어할 수 있습니다.

## 예 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

다음 규칙은 헤더 값이 요청에 변수로 지정된 경우 사용자 지정 헤더를 적용합니다.

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

이 규칙은 HTTP 응답 헤더 `Edge-Control::no-store`을(를) 설정하는 다음 요청에 의해 트리거됩니다.

`http://server/is/image/cat/id?$Edge-Control=no-store`
