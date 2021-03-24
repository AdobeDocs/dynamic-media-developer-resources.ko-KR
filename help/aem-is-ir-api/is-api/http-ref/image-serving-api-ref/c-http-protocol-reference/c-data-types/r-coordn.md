---
description: 정규화된 좌표. 이미지 옵셋 또는 자르기 매개 변수 등의 이미지 내의 상대 위치를 이미지 크기로 정규화하는 데 사용됩니다.
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# coordN{#coordn}

정규화된 좌표. 이미지 옵셋 또는 자르기 매개 변수 등의 이미지 내의 상대 위치를 이미지 크기로 정규화하는 데 사용됩니다.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>이미지의 크기로 정규화된 좌표 오프셋(실제, 실제) </p></td> 
 </tr> 
</table>

양수 값은 오른쪽 아래로 이동합니다.

대부분의 경우 참조 위치가 이미지의 중앙입니다. 이 경우 0,000은 이미지의 중앙에 해당하고, -0.5,-0.5는 왼쪽 위 모서리에 해당하고, 0.5,0.5는 오른쪽 아래 모퉁이에 해당합니다.

레이어 0의 크기를 기준으로 이미지 크기 또는 사각형 크기를 지정하는 데에도 사용됩니다. 이 경우 값은 0보다 커야 합니다. 0은 특정 기본값을 사용해야 함을 나타낼 수 있습니다. 1,1은 레이어 0의 크기와 같은 크기를 지정합니다.
