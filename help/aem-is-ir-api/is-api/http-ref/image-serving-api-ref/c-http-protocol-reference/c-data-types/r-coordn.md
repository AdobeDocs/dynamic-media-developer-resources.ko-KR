---
title: coordN
description: 표준화된 좌표. 이미지 크기에 맞게 표준화된 이미지 오프셋 또는 자르기 매개 변수와 같은 이미지 내의 상대 위치를 지정하는 데 사용됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '148'
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

종종 참조 위치는 이미지의 중심입니다. 이 경우, `0,0` 이미지의 중심에 해당됩니다. `-0.5,-0.5` 왼쪽 상단 모서리로 `0.5,0.5` 오른쪽 하단 모서리입니다.

레이어 0의 크기에 상대적인 이미지 크기 또는 사각형 크기를 지정하는 데에도 사용됩니다. 이 경우 값은 0보다 커야 합니다. 0은 특정 기본값을 사용해야 함을 나타낼 수 있습니다. 값 `1,1` 레이어 0의 크기와 같은 크기를 지정합니다.
