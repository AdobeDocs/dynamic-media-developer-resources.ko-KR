---
description: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eb2196cb-b771-4828-8390-cd9e3fe6c57e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 이미지가 재설정 상태이고 이미지와 상호 작용할 수 있는 동작을 연상시킬 때 <span class="codeph"> iconeffect</span>을(를) 이미지 맨 위에 표시할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 개수</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> iconeffect</span>이(가) 나타나고 다시 나타나는 최대 횟수를 지정합니다. <span class="codeph"> -1</span> 값은 아이콘이 항상 무기한으로 다시 표시됨을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 페이드</span></span> </p> </td> 
   <td colname="col2"> <p>애니메이션을 표시하거나 숨기는 기간(초)을 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 자동 숨기기</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> iconeffect</span>이(가) 자동으로 숨겨지기 전에 완전히 보이는 상태로 유지되는 시간(초)을 설정합니다. 즉, 페이드 인 애니메이션이 완료된 다음 페이드 아웃 애니메이션이 시작되기 전까지의 시간을 의미한다. <span class="codeph"> 0</span> 설정은 자동 숨기기 동작을 사용하지 않도록 설정합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-b6e5e52698d4492f9d6350e7e312bb1b}

선택적.

## 기본값 {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## 예 {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]
