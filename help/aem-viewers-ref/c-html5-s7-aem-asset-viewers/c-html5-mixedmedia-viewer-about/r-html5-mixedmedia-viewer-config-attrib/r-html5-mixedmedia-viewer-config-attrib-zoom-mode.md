---
description: 확대/축소 상호 작용 유형을 설정합니다.
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic,Viewers,SDK/API,혼합 미디어 집합
role: Developer,Business Practitioner
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---

# zoomMode{#zoommode}

확대/축소 상호 작용 유형을 설정합니다.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 연속|인라인|자동  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 연속 </span> 을 사용하면 기본 보기에서 클릭하거나, 두 번 탭하거나, 핀아웃할 때 이미지가 서서히 확대되는 클래식 확대/축소가 가능합니다. 초기 보기로 돌아가려면 확대/축소 상태를 명시적으로 축소하거나 재설정해야 합니다. </p> <p> <span class="codeph"> 인라인 </span> 을 사용하면 즉각적인 확대/축소를 수행할 수 있으며, 여기서 확대/축소된 이미지는 데스크탑의 기본 보기를 가리키거나 터치 장치를 길게 터치할 때 바로 나타납니다.보기에서 마우스를 이동하거나 손가락을 떼면 이미지가 자동으로 초기 상태로 되돌아갑니다. <span class="codeph"> 인라인 </span> 모드 중첩 이미지 세트는 평면화되고 개별 축소판으로 표시됩니다. <span class="codeph"> 자동 </span> 은 데스크탑에서 인라인 모드를 활성화하고 터치 장치에서 연속 모드를 활성화합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-65be9301796240e38f31818229da7acc}

선택 사항입니다.

## 기본값 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 예 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
