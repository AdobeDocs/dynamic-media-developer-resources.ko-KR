---
description: 'text= 렌더러는 크기가 미리 지정된 레이어에 적용할 때 textPs= 렌더러와 근본적으로 다른 텍스트를 배치합니다(예: size=가 지정된 경우에도).'
seo-description: 'text= 렌더러는 크기가 미리 지정된 레이어에 적용할 때 textPs= 렌더러와 근본적으로 다른 텍스트를 배치합니다(예: size=가 지정된 경우에도).'
seo-title: 텍스트 배치
solution: Experience Manager
title: 텍스트 배치
topic: Scene7 Image Serving - Image Rendering API
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 텍스트 배치{#text-positioning}

text= 렌더러는 크기가 미리 지정된 레이어에 적용할 때 textPs= 렌더러와 근본적으로 다른 텍스트를 배치합니다(예: size=가 지정된 경우에도).

자체 크기 조정 `text=`및 `textPs=` 레이어는 모양과 위치가 유사합니다.

`textPs=` 텍스트 상자 경계 밖으로 렌더링된 텍스트 글리프의 일부가 확장되더라도 텍스트 상자 상단에 문자 `\vertalt`셀의 위쪽을 정렬합니다(가정). 특정 글꼴의 렌더링된 글리프는 텍스트 상자의 왼쪽 및 오른쪽 가장자리를 약간 벗어나 돌출될 수도 있습니다. 레이어 사각형 안에 렌더링된 모든 텍스트를 포함시켜야 하는 애플리케이션의 경우 RTF `\marg*` 명령을 사용하거나 텍스트 렌더링 영역을 조정하는 데 사용할 `textFlowPath=` 수 있습니다.

반대로 렌더링된 텍스트는 필요에 따라 `text=` 이동되고 렌더링된 모든 글리프가 지정된 텍스트 상자 내에 완벽하게 어울리도록 보장됩니다.

간단한 애플리케이션에서 좀 더 쉽게 사용할 `text=` 수 있지만 `textPs=` 글꼴 및 텍스트 효과와 상관없이 정확하게 위치를 지정할 수 있습니다.

## 예제 {#section-1b6bdf2ea34447528188ae4e1430ee71}

다음은 사전 크기 텍스트의 예입니다. 자체 크기 텍스트의 동작은 다릅니다.

** `Text=` 항상 맨 위에 좁은 여백을 제공합니다.**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` 텍스트를 텍스트 상자 위쪽에 단단히 정렬하여 렌더링하면 Arial과 같은 일반 글꼴에도 약간 클리핑될 수 있습니다.*

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` 렌더링된 텍스트를 아래로 자동으로 이동하여 클리핑을 방지합니다.**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` 텍스트가 레이어 0:*** 위에 있을 경우 텍스트가 크게 클리핑되는 등 위로 올라오는 부분이 포함된 텍스트는 이동하지 않습니다.

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**맨 위의 10pt(200배) 여백이 클리핑 없이 이 텍스트를 렌더링합니다.**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**특정 스크립트 글꼴의 렌더링된 글리프는 텍스트 상자 외부에서 상당히 확장될 수 있습니다.**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
