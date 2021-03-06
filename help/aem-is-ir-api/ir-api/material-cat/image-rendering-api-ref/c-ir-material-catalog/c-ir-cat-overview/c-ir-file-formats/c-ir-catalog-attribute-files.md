---
description: 카탈로그 특성 파일에는 모든 이름을 사용할 수 있지만 .ini 파일 접미사는 있어야 합니다. 모든 텍스트 편집기를 사용하여 쉽게 유지 관리할 수 있습니다.
solution: Experience Manager
title: 카탈로그 속성 파일
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# 카탈로그 속성 파일{#catalog-attribute-files}

카탈로그 특성 파일에는 모든 이름을 사용할 수 있지만 .ini 파일 접미사는 있어야 합니다. 모든 텍스트 편집기를 사용하여 쉽게 유지 관리할 수 있습니다.

카탈로그 특성 파일은 단일 `<CR>`(ASCII 코드 0xD), 단일 `<LF>`(ASCII 코드 0xA) 또는 `<CR><LF>` 쌍으로 구분된 텍스트 레코드 집합으로 구성됩니다. 각 레코드는 속성 이름과 하나 이상의 쉼표로 구분된 속성 값으로 구성됩니다.

`*``*= *``*&#42;[, *`namevaluvalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 이름  </span> </span> </p> </td> 
  <td class="stentry"> <p>속성 이름; 하나 이상의 문자, 숫자, '-' 및 '_'로 구성될 수 있습니다. 대/소문자를 구분하지 않습니다. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>속성 값; <span class="codeph"> </span> 또는 <span class="codeph"> </span> 문자를 포함하지 않아야 합니다. 단, 줄바꿈 문자 바로 앞에 하나의 백슬래시가 이스케이프 처리되지 않는 한. </p> </td> 
 </tr> 
</table>

* 토큰 간의 공백은 선택 사항입니다.
* 알 수 없는 특성 이름을 사용하는 레코드는 Platform Server에서 무시됩니다.
* 속성 이름은 ASCII 문자, 숫자 및 &quot;-&quot;, &quot;_&quot; 및 &quot;.&quot;의 조합으로 구성될 수 있습니다.
* 동일한 속성 파일에서 동일한 속성 이름이 두 번 이상 발생하면 마지막으로 발생한 속성 이름이 우선합니다.
* 파서가 무시하는 메모로 레코드를 표시하려면 &#39;#&#39;을(를) 첫 번째 문자로 사용하십시오.
