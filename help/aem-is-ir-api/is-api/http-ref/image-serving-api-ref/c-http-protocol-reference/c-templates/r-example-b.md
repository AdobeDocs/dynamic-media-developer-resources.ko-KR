---
description: 예 A와 유사한 요구 사항이지만 단색 배경을 사용하고 다양한 종횡비를 갖는 이미지를 수용하도록 컴포지션의 높이가 달라질 수 있습니다.
solution: Experience Manager
title: 예 B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# 예 B{#example-b}

예 A와 유사한 요구 사항이지만 단색 배경을 사용하고 다양한 종횡비를 갖는 이미지를 수용하도록 컴포지션의 높이가 달라질 수 있습니다.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 카탈로그::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 카탈로그::수정자</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

이미지는 레이어 0에 배치되고 높이 값 `size=`이 0으로 설정되면 실제 높이는 800픽셀로 크기를 조절한 후 이미지의 높이에 의해 결정됩니다.

`extend=` 위쪽 및 아래쪽에는 100픽셀이, 오른쪽에는 200픽셀이 추가됩니다.

두 레이어 0과 레이어 1의 원점은 합성 영역의 오른쪽 중앙에 배치되어 원하는 텍스트 위치를 얻습니다.

다음 그림은 이미지의 다른 종횡비와 다른 텍스트 문자열의 합성 결과를 보여줍니다.

![](assets/exampleb.png)
