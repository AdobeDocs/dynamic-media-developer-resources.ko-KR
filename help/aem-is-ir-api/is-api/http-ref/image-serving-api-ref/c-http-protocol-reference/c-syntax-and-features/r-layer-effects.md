---
title: 레이어 효과
description: Photoshop 스타일 레이어 그림자 및 광선 효과는 layer=0 및 layer=comp를 포함하여 모든 레이어(상위 레이어)에 첨부할 수 있는 특수 하위 레이어(효과 레이어)를 사용하여 구현됩니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f99bb3d-c5d6-4215-a76b-58ba7689ff02
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 2%

---

# 레이어 효과{#layer-effects}

Photoshop 스타일 레이어 그림자 및 광선 효과는 layer=0 및 layer=comp를 포함하여 모든 레이어(상위 레이어)에 첨부할 수 있는 특수 하위 레이어(효과 레이어)를 사용하여 구현됩니다.

효과 레이어는 다양한 표준 이미지와 레이어 특성 및 명령을 지원하지만 일반적인 목적의 레이어는 아니며, 독립적인 이미지 또는 텍스트 데이터를 지원하지 않습니다.

여러 레이어 효과를 하나의 부모 레이어에 첨부할 수 있습니다.

## 내부 및 외부 효과 {#section-2dade7ee98e041d1b4d1725e6f98a515}

*내부 효과* 은 부모 레이어의 맨 위에 렌더링되며 부모 레이어의 불투명 영역에서만 볼 수 있습니다. *외부 효과* 는 상위 레이어 뒤에 렌더링되어(따라서 상위 레이어의 불투명 영역 내에서는 표시되지 않음) 합성 캔버스 내 어디에나 배치할 수 있습니다. 내부 또는 외부 효과는 양수 또는 음수 효과 레이어 번호에 `effect=` 명령입니다. 다음 `effect=` 또한 명령은 동일한 부모 레이어에 첨부된 여러 효과 레이어 간의 z 순서 지정을 제어합니다.

## 상위 계층에 대한 관계 {#section-eb8bfc4f754a42fc973b562821d6f2d3}

효과 레이어는 자동으로 크기가 조정되고 부모 레이어와 일치하도록 배치됩니다(즉, 효과 레이어가 `size=` 및 `origin=` 상위 레이어의 값). `pos=` 일반적으로 드롭 및 내부 그림자 효과에 필요한 대로 효과 레이어를 부모 레이어에서 멀리 이동하는 데 사용할 수 있습니다. 표준 레이어의 경우 `pos=` 효과 레이어의 경우 이 레이어와 레이어 0 사이의 오프셋을 지정합니다. `pos=` 효과 레이어와 부모 레이어의 원본 사이의 오프셋을 지정합니다.

## 지원되는 명령 및 속성 {#section-035fc6bcba7d4e7ab4bd46687c1d8879}

효과 레이어에는 다음과 같은 명령과 특성이 적용됩니다.

* `blendMode=`
* `effect=`
* `color=`
* `maskUse=`
* `opac=`
* `op_grow=`
* `op_blur=`
* `op_noise=`
* `pos=`

효과 레이어에 포함된 다른 모든 이미지 및 레이어 명령은 무시됩니다.

## 기본 효과 매크로 {#section-a01e8dcc87c94495b54a6dfb21d2a718}

레이어 효과를 쉽게 사용할 수 있도록 IS는 기본 이미지 카탈로그와 함께 두 개의 매크로를 제공합니다. `$shadow$` 및 `$glow$`: Photoshop 레이어 효과와 유사한 효과 레이어 속성에 대한 기본값을 제공합니다. 다음 표에는 기본 레이어 효과를 구현하는 데 사용해야 하는 효과 명령과 매크로가 나와 있습니다. 매크로에 지정된 모든 특성을 URL에서 수정하거나 대체 매크로를 만들어 사용자 정의 레이어 효과를 구현할 수 있습니다.

<table id="table_8089C41AD1F24223A58C7DD8F4DDF73C"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 원하는 효과</b> </th> 
   <th class="entry"> <b> 명령</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> 그림자 효과 </p> </td> 
   <td> <p> <span class="codeph"> 효과=-1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 내부 그림자 </p> </td> 
   <td> <p> <span class="codeph"> 효과=1&amp;$shadow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 외부 광선 </p> </td> 
   <td> <p> <span class="codeph"> 효과=-1&amp;$glow$</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 내부 광선 </p> </td> 
   <td> <p> <span class="codeph"> 효과=1&amp;$glow$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 예제 {#section-4c449fdf707b43858917fb271fa1fe96}

레이어에 불투명도가 50%인 세 픽셀 너비의 빨간색 테두리를 추가합니다.

`…&effect=-1&op_grow=3&color=255,0,0,128&…`

테두리는 이미지의 알파 채널 또는 마스크의 윤곽선을 따릅니다. 설정 `effect=1` 는 대신 내부 가장자리에 테두리를 배치합니다.

기본 효과 설정(색상 제외)을 사용하여 이미지에 파랑 그림자를 추가합니다.

[!DNL http://server/is/image/myCat/myImage?size=200,200&extend=0,0,10,10&effect=-1&$shadow$&color=50,143,254]

`extend=` 이미지의 오른쪽 아래 가장자리에 여백을 약간 추가하여 그림자가 이미지 경계와 잘리지 않도록 합니다.

## 참조 {#section-1acccccf534549aea23d4c008c17e7c0}

[효과=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135), [명령 매크로%l94560](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-command-macros.md#reference-ea2a9571c65a46da83eca27d0013cbf9)
