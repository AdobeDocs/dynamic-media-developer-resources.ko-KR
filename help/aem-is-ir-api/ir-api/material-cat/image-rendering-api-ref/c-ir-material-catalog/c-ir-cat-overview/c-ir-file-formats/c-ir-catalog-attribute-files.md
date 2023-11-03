---
title: 카탈로그 속성 파일
description: 카탈로그 속성 파일의 이름은 모두 지정할 수 있지만 .ini 파일 접미사가 있어야 합니다. 텍스트 편집기를 사용하여 쉽게 유지 관리할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# 카탈로그 속성 파일{#catalog-attribute-files}

카탈로그 속성 파일의 이름은 무엇이든 지정할 수 있지만 `.ini` 파일 접미사. 텍스트 편집기를 사용하여 쉽게 유지 관리할 수 있습니다.

카탈로그 속성 파일은 텍스트 레코드 세트로 구성되며, 하나로 구분됩니다 `<CR>` (ASCII 코드 0xD), 단일 `<LF>` (ASCII 코드 0xA) 또는 `<CR><LF>` 짝을 지어 각 레코드는 속성 이름과 하나 이상의 쉼표로 구분된 속성 값으로 구성됩니다.

`*`이름`*= *`값`*&#42;[, *`값`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 이름 </span> </span> </p> </td> 
  <td class="stentry"> <p>속성 이름, 하나 이상의 문자, 숫자, '-' 및 '_'로 구성될 수 있으며 대소문자를 구분하지 않습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 값 </span> </span> </p> </td> 
  <td class="stentry"> <p>속성 값, 다음을 포함하지 않음 <span class="codeph"> &lt;cr&gt; </span>, 또는 <span class="codeph"> &lt;lf&gt; </span> 줄 바꿈 문자 바로 앞에 단일 백슬래시로 이스케이프되지 않는 한 문자를 사용할 수 있습니다. </p> </td> 
 </tr> 
</table>

* 토큰 사이의 공백은 선택 사항입니다.
* 알 수 없는 속성 이름을 가진 레코드는 [!DNL Platform Server].
* 속성 이름은 ASCII 문자, 숫자 및 &quot;-&quot;, &quot;_&quot;, &quot;.&quot;의 모든 조합으로 구성될 수 있습니다.
* 동일한 속성 이름이 동일한 속성 파일에서 두 번 이상 발생하면 마지막으로 발생한 이름이 우선합니다.
* 파서가 무시하는 주석으로 레코드를 표시하려면 &#39;#&#39;를 첫 번째 문자로 사용하십시오.
