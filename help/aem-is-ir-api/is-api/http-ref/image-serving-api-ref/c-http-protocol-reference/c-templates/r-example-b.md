---
description: 예제 A와 유사한 요구 사항이지만 단색 배경을 사용하고 다른 종횡비를 사용하는 이미지를 수용하기 위해 합성 높이를 다르게 할 수 있습니다.
seo-description: 예제 A와 유사한 요구 사항이지만 단색 배경을 사용하고 다른 종횡비를 사용하는 이미지를 수용하기 위해 합성 높이를 다르게 할 수 있습니다.
seo-title: 예 B
solution: Experience Manager
title: 예 B
topic: Scene7 Image Serving - Image Rendering API
uuid: 13120562-9201-4733-bd9d-4a54eac913e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# 예 B{#example-b}

예제 A와 유사한 요구 사항이지만 단색 배경을 사용하고 다른 종횡비를 사용하는 이미지를 수용하기 위해 합성 높이를 다르게 할 수 있습니다.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 카탈로그::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 카탈로그::수정자</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+gops+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;originN=.5,5 0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

이 이미지는 레이어 0에 배치되고, 높이 값 `size=`은 0으로 설정되므로, 실제 높이는 800픽셀로 크기를 조절한 후 이미지의 높이에 따라 결정됩니다.

`extend=` 위쪽과 아래쪽에 100픽셀을 추가하고 오른쪽에는 200픽셀을 추가합니다.

레이어 0과 레이어 1의 원점은 합성 영역의 오른쪽 중앙에 배치되므로 원하는 텍스트 위치를 얻을 수 있습니다.

다음 그림은 이미지의 다양한 종횡비와 다른 텍스트 문자열에 대한 합성 결과를 보여줍니다.

![](assets/exampleb.png)

