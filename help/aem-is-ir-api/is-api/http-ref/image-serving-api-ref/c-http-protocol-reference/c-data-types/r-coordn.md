---
description: 표준화된 좌표. 이미지 크기에 맞게 표준화된 이미지 오프셋 또는 자르기 매개 변수와 같은 이미지 내의 상대 위치를 지정하는 데 사용됩니다.
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# coordN{#coordn}

표준화된 좌표. 이미지 크기에 맞게 표준화된 이미지 오프셋 또는 자르기 매개 변수와 같은 이미지 내의 상대 위치를 지정하는 데 사용됩니다.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>이미지 크기(실수, 실수)로 정규화된 좌표 오프셋 </p></td> 
 </tr> 
</table>

양수 값은 오른쪽 아래로 이동합니다.

많은 경우, 기준 위치는 이미지의 중심입니다. 이 경우 0,0은 이미지의 중앙에 해당하고, 왼쪽 위 모서리에는 -0.5,-0.5, 오른쪽 아래 모서리에는 0.5,0.5가 해당합니다.

레이어 0의 크기를 기준으로 이미지 크기나 사각형 크기를 지정하는 데에도 사용됩니다. 이 경우 값은 0보다 커야 합니다. 0은 특정 기본값을 사용해야 함을 나타낼 수 있습니다. 1,1은 레이어 0과 같은 크기를 지정합니다.
