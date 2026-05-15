---
description: 카탈로그 속성 파일의 이름은 모두 지정할 수 있지만 .ini 파일 접미사가 있어야 합니다. 텍스트 편집기를 사용하여 쉽게 유지 관리할 수 있습니다.
solution: Experience Manager
title: 카탈로그 속성 파일
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
TQID: 'https://experienceleague.adobe.com/RCxeXg3wb10jo37biAs1puqmEo8bAL-i-oZBwGHuloA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 0%

---

# 카탈로그 속성 파일{#catalog-attribute-files}

카탈로그 속성 파일의 이름은 모두 지정할 수 있지만 .ini 파일 접미사가 있어야 합니다. 텍스트 편집기를 사용하여 쉽게 유지 관리할 수 있습니다.

카탈로그 특성 파일은 단일 `<CR>`(ASCII 코드 `0xD`), 단일 `<LF>`(ASCII 코드 `0xA`) 또는 `<CR><LF>` 쌍으로 구분된 텍스트 레코드 집합으로 구성됩니다. 각 레코드는 속성 이름과 하나 이상의 쉼표로 구분된 속성 값으로 구성됩니다.

`*`이름`*= *`값`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">개 값</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 값</span>[,<span class="varname"> 값</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 이름</span> </p> </td> 
  <td class="stentry"> <p>속성 이름. 하나 이상의 문자, 숫자, -, _ 로 구성될 수 있습니다. 대/소문자를 구분하지 않습니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 값</span> </p></td> 
  <td class="stentry"> <p>속성 값입니다. 줄 바꿈 문자 바로 앞에 단일 백슬래시로 이스케이프되지 않는 한 <span class="codeph"> &lt;CR&gt;</span> 또는 <span class="codeph"> &lt;LF&gt;</span>자를 포함해서는 안 됩니다. </p></td> 
 </tr> 
</table>

토큰 사이의 공백은 선택 사항입니다.

알 수 없는 특성 이름이 있는 레코드는 [!DNL Platform Server]에서 무시됩니다.

속성 이름은 ASCII 문자, 숫자와 &quot;-&quot;, &quot;_&quot; 및 &quot;.&quot;의 모든 조합으로 구성될 수 있습니다.

동일한 속성 이름이 동일한 속성 파일에서 두 번 이상 발생하면 마지막으로 발생한 이름이 우선합니다.

파서에서 무시하는 모든 레코드를 주석으로 표시하려면 #을 첫 번째 문자로 사용합니다.
