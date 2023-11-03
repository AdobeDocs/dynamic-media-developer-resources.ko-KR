---
title: 텍스트 위치
description: text= 렌더러는 미리 크기가 지정된 레이어에 적용할 때(즉, size=가 지정된 경우) textPs= 렌더러와 근본적으로 다른 텍스트를 배치합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# 텍스트 위치{#text-positioning}

다음 `text=` 렌더러는 미리 크기가 지정된 레이어에 적용할 때(즉, size=가 지정된 경우) textPs= 렌더러와 근본적으로 다른 텍스트를 배치합니다.

자가 크기 조정 `text=`및 `textPs=` 레이어는 비슷한 모양과 위치를 갖습니다.

다음 `textPs=` 문자 셀의 위쪽을 텍스트 상자의 위쪽에 맞춥니다( `\vertalt`) 렌더링하면 텍스트 상자 경계 밖으로 부분적으로 확장되는 렌더링된 텍스트 글리프의 일부가 되더라도 특정 글꼴의 렌더링된 글리프가 텍스트 상자의 왼쪽 및 오른쪽 가장자리를 약간 벗어나 돌출할 수도 있습니다. 렌더링된 모든 텍스트를 레이어 사각형 내에 포함해야 하는 응용 프로그램의 경우 RTF가 `\marg*` 명령 또는 `textFlowPath=` 를 사용하여 텍스트 렌더링 영역을 조정할 수 있습니다.

대조적으로, `text=` 필요한 경우 렌더링된 텍스트를 이동하고 렌더링된 모든 글리프가 지정된 텍스트 상자 내에 완전히 맞도록 합니다.

While `text=` 간단한 응용 프로그램에 약간 더 쉽게 사용할 수 있습니다. `textPs=` 에서는 글꼴 및 텍스트 효과에 관계없이 정확한 위치를 제공합니다.

## 예제 {#section-1b6bdf2ea34447528188ae4e1430ee71}

다음 예제는 미리 크기가 조정된 텍스트에 대한 것입니다. 자체 크기 조정 텍스트에 대한 동작이 다릅니다.

** `Text=` 항상 맨 위에 좁은 여백을 제공합니다.**

![텍스트 위치 지정 예 1 이미지](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` 는 텍스트 상자의 위쪽에 텍스트를 촘촘하게 정렬하여 Arial®:**과 같은 일반적인 글꼴에 대해서도 약간의 클리핑을 생성합니다.

![텍스트 위치 지정 예제 2 이미지](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` 렌더링된 텍스트를 아래로 자동 이동하여 클리핑 방지:**

![텍스트 위치 지정 예제 3 이미지](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` 볼록 부분이 포함된 텍스트를 이동하지 않으므로 텍스트가 레이어 0:**에 있는 경우 상당한 클리핑이 발생합니다.

![텍스트 위치 지정 예 4 이미지](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**상단의 10pt(200트윕) 여백은 클리핑 없이 이 텍스트를 렌더링합니다.**

![텍스트 위치 지정 예 5 이미지](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**특정 스크립트 글꼴의 렌더링된 글리프가 텍스트 상자 밖으로 상당히 확장될 수 있습니다.**

![텍스트 위치 지정 예 6 이미지](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
