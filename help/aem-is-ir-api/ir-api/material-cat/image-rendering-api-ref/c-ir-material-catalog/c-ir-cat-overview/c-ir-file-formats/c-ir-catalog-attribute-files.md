---
description: 카탈로그 특성 파일은 모든 이름을 가질 수 있지만 .ini 파일 접미어를 사용해야 합니다. 텍스트 편집기를 사용하여 언제든지 유지 관리할 수 있습니다.
seo-description: 카탈로그 특성 파일은 모든 이름을 가질 수 있지만 .ini 파일 접미어를 사용해야 합니다. 텍스트 편집기를 사용하여 언제든지 유지 관리할 수 있습니다.
seo-title: 카탈로그 속성 파일
solution: Experience Manager
title: 카탈로그 속성 파일
topic: Scene7 Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# 카탈로그 특성 파일{#catalog-attribute-files}

카탈로그 특성 파일은 모든 이름을 가질 수 있지만 .ini 파일 접미어를 사용해야 합니다. 텍스트 편집기를 사용하여 언제든지 유지 관리할 수 있습니다.

카탈로그 속성 파일은 단일 `<CR>`(ASCII 코드 0xD), 단일 `<LF>`(ASCII 코드 0xA) 또는 `<CR><LF>` 쌍으로 구분된 텍스트 레코드 세트로 구성됩니다. 각 레코드는 속성 이름과 하나 이상의 쉼표로 구분된 속성 값으로 구성됩니다.

` *``*= *``*&#42;[, *`이름 평가값`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>속성 이름;은 하나 이상의 문자, 숫자, '-' 및 '_'로 구성됩니다.대/소문자를 구분하지 않습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>속성 값;줄바꿈 문자 바로 앞에 하나의 백슬래시로 이스케이프되지 않는 한 <span class="codeph"> </span> 또는 <span class="codeph"> </span> 문자를 포함할 수 없습니다. </p> </td> 
 </tr> 
</table>

* 토큰 사이의 공백은 선택 사항입니다.
* 알 수 없는 특성 이름의 레코드는 플랫폼 서버에서 무시됩니다.
* 속성 이름은 ASCII 문자, 숫자와 &quot;-&quot;, &quot;_&quot; 및 &quot;.&quot;의 조합으로 구성될 수 있습니다.
* 동일한 속성 파일에서 동일한 속성 이름이 두 번 이상 발생하면 마지막으로 발견된 속성 이름이 우선합니다.
* &#39;#&#39;을(를) 첫 번째 문자로 사용하여 파서가 무시하는 주석으로 레코드를 표시합니다.

