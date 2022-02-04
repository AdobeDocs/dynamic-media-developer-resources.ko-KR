---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 40b7887d-d525-4816-8c72-9ef8f5948de3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`페이드`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 를 활성화합니다 <span class="codeph"> 아이콘 효과</span> 이미지가 재설정 상태일 때 이미지 맨 위에 표시하기 위해, 이미지와 상호 작용하는 사용 가능한 작업이 표시됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 계수</span></span> </p> </td> 
   <td colname="col2"> <p> 최대 횟수를 지정합니다. <span class="codeph"> 아이콘 효과</span> 나타납니다. 값 <span class="codeph"> -1</span> 아이콘이 항상 무한정 다시 표시됨을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 페이드</span></span> </p> </td> 
   <td colname="col2"> <p>애니메이션 표시 또는 숨기기 지속 시간을 초 단위로 지정합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>에서 <span class="codeph"> 아이콘 효과</span> 자동으로 숨겨지기 전에 완전히 보이도록 유지합니다. 즉, 페이드 인 애니메이션이 완료된 후 페이드 아웃 애니메이션이 시작되기 전 시간입니다. 설정 <span class="codeph"> 0</span> 자동 숨기기 동작을 비활성화합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
