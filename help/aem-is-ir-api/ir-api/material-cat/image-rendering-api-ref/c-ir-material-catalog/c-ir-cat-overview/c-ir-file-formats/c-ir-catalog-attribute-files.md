---
description: 카탈로그 속성 파일에는 어떤 이름이든 사용할 수 있지만 .ini 파일 접미어를 사용해야 합니다. 모든 텍스트 편집기를 사용하여 손쉽게 유지 관리할 수 있습니다.
seo-description: 카탈로그 속성 파일에는 어떤 이름이든 사용할 수 있지만 .ini 파일 접미어를 사용해야 합니다. 모든 텍스트 편집기를 사용하여 손쉽게 유지 관리할 수 있습니다.
seo-title: 카탈로그 속성 파일
solution: Experience Manager
title: 카탈로그 속성 파일
topic: Scene7 Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 카탈로그 속성 파일{#catalog-attribute-files}

카탈로그 속성 파일에는 어떤 이름이든 사용할 수 있지만 .ini 파일 접미어를 사용해야 합니다. 모든 텍스트 편집기를 사용하여 손쉽게 유지 관리할 수 있습니다.

카탈로그 속성 파일은 단일 `<CR>` (ASCII 코드 0xD), 단일 `<LF>` (ASCII 코드 0xA) 또는 `<CR><LF>` 쌍으로 구분된 텍스트 레코드 세트로 구성됩니다. 각 레코드는 속성 이름과 하나 이상의 쉼표로 구분된 속성 값으로 구성됩니다.

` *``*= *``*&#42;[, *`이름 평가`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 이름 </span></span> </p> </td> 
  <td class="stentry"> <p>속성 이름;은 하나 이상의 문자, 숫자, '-' 및 '_'로 구성됩니다.대/소문자를 구분하지 않습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 값 </span></span> </p> </td> 
  <td class="stentry"> <p>속성 값;줄바꿈 문자 바로 앞에 <span class="codeph"> &lt;CR&gt; </span>또는 <span class="codeph"> &lt;LF&gt; </span> 문자를 사용하지 않아야 합니다. 단, 한 개의 백슬래시로 이스케이프되지 않아야 합니다. </p> </td> 
 </tr> 
</table>

* 토큰 사이의 공백은 선택 사항입니다.
* 알 수 없는 속성 이름을 가진 레코드는 플랫폼 서버에서 무시됩니다.
* 속성 이름은 ASCII 문자, 숫자와 &quot;-&quot;, &quot;_&quot; 및 &quot;.&quot;의 조합으로 구성될 수 있습니다.
* 동일한 속성 파일에서 동일한 속성 이름이 두 번 이상 발생하는 경우 마지막으로 발견된 속성 이름이 우선합니다.
* &#39;#&#39;을(를) 첫 번째 문자로 사용하여 모든 레코드를 구문 분석기가 무시하는 주석으로 표시합니다.

