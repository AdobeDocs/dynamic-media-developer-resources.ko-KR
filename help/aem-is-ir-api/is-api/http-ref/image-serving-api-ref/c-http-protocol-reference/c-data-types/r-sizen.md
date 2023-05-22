---
description: 정규화된 크기입니다. 레이어 0 또는 일부 다른 이미지의 크기를 기준으로 표준화된 이미지 크기 또는 사각형 크기를 지정하는 데 사용됩니다.
solution: Experience Manager
title: 크기 N
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# 크기 N{#sizen}

정규화된 크기입니다. 레이어 0 또는 일부 다른 이미지의 크기를 기준으로 표준화된 이미지 크기 또는 사각형 크기를 지정하는 데 사용됩니다.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 크기 N</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>다른 이미지에 상대적인 표준화된 너비 및 높이(실수, 실수, 0보다 큼) </p></td> 
 </tr> 
</table>

모두 *nx* 및 *ny* 은(는) 0보다 커야 합니다. 0,0은 특정 기본 크기를 사용해야 함을 나타낼 수 있습니다. 1,1은 참조 이미지와 같은 크기를 지정합니다.
