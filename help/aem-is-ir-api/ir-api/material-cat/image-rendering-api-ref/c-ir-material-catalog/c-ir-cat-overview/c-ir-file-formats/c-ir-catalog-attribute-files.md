---
title: 카탈로그 속성 파일
description: 카탈로그 속성 파일의 이름은 모두 지정할 수 있지만 .ini 파일 접미사가 있어야 합니다. 텍스트 편집기를 사용하여 쉽게 유지 관리할 수 있습니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# 카탈로그 속성 파일{#catalog-attribute-files}

카탈로그 특성 파일의 이름은 모두 지정할 수 있지만 `.ini` 파일 접미사가 있어야 합니다. 텍스트 편집기를 사용하여 쉽게 유지 관리할 수 있습니다.

카탈로그 특성 파일은 단일 `<CR>`(ASCII 코드 0xD), 단일 `<LF>`(ASCII 코드 0xA) 또는 `<CR><LF>` 쌍으로 구분된 텍스트 레코드 집합으로 구성됩니다. 각 레코드는 속성 이름과 하나 이상의 쉼표로 구분된 속성 값으로 구성됩니다.

`*`이름`*= *`값`*&#42;[, *`값`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 이름 </span> </span> </p> </td> 
  <td class="stentry"> <p>속성 이름, 하나 이상의 문자, 숫자, -(하이픈) 및 _(밑줄)로 구성될 수 있으며 대소문자를 구분하지 않습니다.</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 값 </span> </span> </p> </td> 
  <td class="stentry"> <p>특성 값; 줄 바꿈 문자 바로 앞에 백슬래시 한 개로 이스케이프하지 않는 한 <span class="codeph"> &lt;CR&gt; </span> 또는 <span class="codeph"> &lt;LF&gt; </span>자를 포함해서는 안 됩니다. </p> </td> 
 </tr> 
</table>

* 토큰 사이의 공백은 선택 사항입니다.
* [!DNL Platform Server]은(는) 알 수 없는 특성 이름이 있는 레코드를 무시합니다.
* 특성 이름은 ASCII 문자, 숫자 및 `-`, `_`, `.`자의 조합으로 구성될 수 있습니다.
* 동일한 속성 이름이 동일한 속성 파일에서 두 번 이상 발생하면 마지막으로 발생한 이름이 우선합니다.
* 파서가 무시하는 주석으로 레코드를 표시하려면 `#`을(를) 첫 번째 문자로 사용하십시오.
