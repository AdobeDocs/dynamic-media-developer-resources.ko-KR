---
description: 카탈로그 특성 파일에는 모든 이름을 사용할 수 있지만 .ini 파일 접미사는 있어야 합니다. 모든 텍스트 편집기를 사용하여 쉽게 유지 관리할 수 있습니다.
solution: Experience Manager
title: 카탈로그 속성 파일
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# 카탈로그 속성 파일{#catalog-attribute-files}

카탈로그 특성 파일에는 모든 이름을 사용할 수 있지만 .ini 파일 접미사는 있어야 합니다. 모든 텍스트 편집기를 사용하여 쉽게 유지 관리할 수 있습니다.

카탈로그 속성 파일은 텍스트 레코드 집합으로 구성되며 단일 `<CR>` (ASCII 코드) `0xD`), 단일 `<LF>` (ASCII 코드) `0xA`) 또는 `<CR><LF>` 한 개. 각 레코드는 속성 이름과 하나 이상의 쉼표로 구분된 속성 값으로 구성됩니다.

`*`이름`*= *`값`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> 값</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 이름</span> </p> </td> 
  <td class="stentry"> <p>속성 이름입니다. 하나 이상의 문자, 숫자, - 및 _ 로 구성될 수 있습니다. 대/소문자를 구분하지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>속성 값. 다음을 포함하지 않아야 합니다 <span class="codeph"> &lt;cr&gt;</span> 또는 <span class="codeph"> &lt;lf&gt;</span> 단일 백슬래시로 이스케이프되지 않은 경우 줄바꿈 문자 바로 앞에 문자가 옵니다. </p></td> 
 </tr> 
</table>

토큰 간의 공백은 선택 사항입니다.

알 수 없는 속성 이름을 사용하는 레코드는 [!DNL Platform Server].

속성 이름은 &quot;-&quot;, &quot;_&quot; 및 &quot;.&quot;와 같은 ASCII 문자, 숫자 조합으로 구성될 수 있습니다.

동일한 속성 파일에서 동일한 속성 이름이 두 번 이상 발생하면 마지막으로 발생한 속성 이름이 우선합니다.

레코드를 메모로 표시하려면 # 을 첫 번째 문자로 사용하십시오. 이 경우 파서는 무시됩니다.
