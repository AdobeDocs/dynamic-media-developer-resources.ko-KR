---
description: 정적 배경 이미지, 왼쪽 중앙에 배경에 정렬되어 배경의 폭과 높이의 80%를 초과하지 않도록 크기가 조정된 변수 이미지, 캔버스 오른쪽 가장자리에 가운데에 세로 텍스트가 있는 텍스트 레이어를 포함하여 고정 크기를 만듭니다.
solution: Experience Manager
title: 예 A
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# 예 A{#example-a}

정적 배경 이미지, 왼쪽 중앙에 배경에 정렬되어 배경의 폭과 높이의 80%를 초과하지 않도록 크기가 조정된 변수 이미지, 캔버스 오른쪽 가장자리에 가운데에 세로 텍스트가 있는 텍스트 레이어를 포함하여 고정 크기를 만듭니다.

![](assets/examplea.png)

## 템플릿 레코드 {#section-32f54710593e438fa0622224c89380af}

개체 삽입

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 카탈로그::Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 카탈로그::수정자  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=100,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp;posN=-0.5,0&amp;px&amp;layer=2&amp;$text=layer+2+text+gots+go+here&amp;text=rtf...$text$...rtf-encoding&amp;r&amp;retp&amp;R0&amp;N=90&amp;origin=0.0.5,0.5,0.0.0&amp;prop.0.5,0.0.0.5,0.5,0&amp;pos.0.0.0.5,0&amp;pos  </span> </p> </td> 
 </tr> 
</table>

모든 레이어의 `origin=` 값은 레이어의 배치 및 정렬을 엄격히 제어하기 위해 템플릿에 명시적으로 지정됩니다. 각 레이어 원점은 해당 레이어에 대해 원하는 맞춤과 일치하도록 설정됩니다. 배경(레이어 0)의 `origin=`이 가운데로 설정됩니다.이는 런타임 시 배경 이미지가 변경되지 않으므로 임의적입니다.레이어 0 원점에 대한 모든 값을 사용할 수 있습니다.

`pos=` 값은 원하는 레이어 위치를 얻기 위해 레이어 원점 간에 필요한 오프셋을 제공합니다.

레이어 1 이미지의 앵커는 왼쪽 중앙에 배치됩니다.`pos=` 값과 함께 사용하면 레이어 1 이미지의 종횡비에 관계없이 배경 이미지와 레이어 1 이미지 간의 왼쪽 가운데 맞춤이 수행됩니다.

마찬가지로 텍스트 레이어의 앵커는 자동 크기 텍스트 상자의 오른쪽 중앙에 배치됩니다. pos와 함께= 글꼴 크기 및 문자열 길이와 관계없이 회전된 텍스트에 대해 원하는 오른쪽 가운데 맞춤을 수행합니다.

실제 표시 텍스트는 런타임 시 제공되므로 변수를 사용하여 텍스트를 rtf 서식 봉투와 구분합니다. 레이어 1 이미지에 기본 변수 `$object`을 사용합니다. 이렇게 하면 요청 경로에서 이 이미지를 지정할 수 있습니다.

배경 이미지와 레이어 1 이미지에 모든 이미지를 사용할 수 있습니다. 배경 이미지에 마스크가 있으면 마스크되지 않은 영역이 기본 배경색( `attribute::BkgColor`)으로 채워지거나 `fmt=png-alpha` 또는 `fmt=tif-alpha`일 때 왼쪽 투명으로 채워집니다. 배경 이미지에 정사각형이 아닌 종횡비가 있는 경우 이 이미지는 회신 이미지의 가운데에 표시되고 추가 공간은 `attribute::BkgColor` 로 채워집니다. 레이어 1 이미지에 알파 데이터 또는 마스크가 있으면 배경 이미지(또는 배경색)가 투명 영역에 계속 표시됩니다. 이미지에 마스크가 없으면 할당된 전체 사각형이 채워집니다.

## 템플릿 사용 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`서버`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

다음 그림은 레이어 1 이미지와 다른 텍스트 문자열의 다른 종횡비에 대한 복합 결과를 보여줍니다.

![](assets/exampleausing.png)
