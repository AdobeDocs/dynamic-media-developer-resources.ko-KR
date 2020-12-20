---
description: 자산에 대한 게시 컨텍스트 상태를 업데이트합니다.
seo-description: 자산에 대한 게시 컨텍스트 상태를 업데이트합니다.
seo-title: ContextStateUpdate
solution: Experience Manager
title: ContextStateUpdate
topic: Scene7 Image Production System API
uuid: ef579d3c-1899-4088-903e-e6ed5a414ca8
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 8%

---


# ContextStateUpdate{#contextstateupdate}

자산에 대한 게시 컨텍스트 상태를 업데이트합니다.

구문

## 매개 변수 {#section-9f747df071854c6896fdbb95684ad947}

자산의 게시 컨텍스트 상태를 `setAssetsContextState`으로 설정합니다.

<table id="table_FD172CEA4EFE44E08ADA22D090DC06CA">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 이름 </th>
   <th colname="col2" class="entry"> 유형 </th>
   <th colname="col3" class="entry"> 설명 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextHandle</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:문자열 </span></td>
   <td colname="col3"> 게시 컨텍스트를 처리합니다. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> publishState</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:문자열</span></td>
   <td colname="col3">지정된 게시 컨텍스트에 대해 자산의 업데이트된 게시 상태입니다. 포함: 
    <ul id="ul_CF6019C4CA3648B687C252F1A7C2EAAF">
     <li id="li_4367D7A058F045D98CDF58009E2AC7BC"><span class="codeph"> MarkedForPublish</span></li>
     <li id="li_EEFC6A76C1014C6D9D5E66F271B68606"><span class="codeph"> NotMarkedForPublish</span></li>
     <li id="li_5145CFA39F5249C48DBD0A37543AF055"><span class="codeph"></span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [게시 상태](../../string-constants/c-string-constants/r-publish-state.md#reference-a9d80231514b4272b39d10c1a7aadca8)

