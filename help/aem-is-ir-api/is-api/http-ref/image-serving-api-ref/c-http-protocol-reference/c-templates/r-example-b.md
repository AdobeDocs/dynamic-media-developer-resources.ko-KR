---
description: 예제 A와 유사한 요구 사항을 만족하지만 단색 배경을 사용하고 컴포지트의 높이를 변경하여 다른 종횡비의 이미지를 수용할 수 있습니다.
solution: Experience Manager
title: 예 B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# 예 B{#example-b}

예제 A와 유사한 요구 사항을 만족하지만 단색 배경을 사용하고 컴포지트의 높이를 변경하여 다른 종횡비의 이미지를 수용할 수 있습니다.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 카탈로그::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 카탈로그::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf..$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

이미지가 레이어 0에 배치되고 높이 값 `size=`이(가) 0으로 설정됩니다. 이 설정을 사용하면 너비를 800픽셀로 조절한 후 이미지의 높이에 따라 실제 높이가 결정됩니다.

변수 `extend=`은(는) 위쪽과 아래쪽에 100픽셀을 추가하고 오른쪽에 200픽셀을 추가합니다.

레이어 0과 레이어 1의 원점은 원하는 텍스트 위치를 얻기 위해 합성 영역의 오른쪽 가운데에 배치됩니다.

다음 이미지는 이미지와 텍스트 문자열의 서로 다른 종횡비에 대한 합성 결과를 보여 줍니다.

![예제 B 이미지](assets/exampleb.png)
