---
title: 클립 경로
description: 레이어 클립 패스. 현재 레이어의 클립 경로를 지정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# 클립 경로{#clippath}

레이어 클립 패스. 현재 레이어의 클립 경로를 지정합니다.

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>경로 데이터. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>레이어 소스 이미지에 포함된 경로 이름(ASCII만 해당). </p></td> 
 </tr> 
</table>

`clipPath=`에 의해 정의된 영역 밖에 있는 레이어의 모든 부분이 투명하게 렌더링됩니다.

`*`pathName`*`은(는) 레이어 원본 이미지에 포함된 경로 이름입니다. 이미지 내용과의 상대 정렬을 유지하기 위해 경로가 자동으로 변형됩니다. 두 개 이상의 `*`pathName`*`을(를) 지정하면 서버에서 이미지를 이러한 경로의 교차 지점으로 클리핑합니다. 원본 이미지에서 찾을 수 없는 `*`pathName`*`은(는) 무시됩니다.

>[!NOTE]
>
>`*`pathName`*`에는 ASCII 문자열만 지원됩니다.

`*`pathDefinition`*`에서 레이어 픽셀 좌표에 명시적 경로 데이터를 지정할 수 있습니다.

`size=`이(가) 지정되고 0,0이(가) 아닌 경우 레이어가 적용됩니다. 이 경우 경로 좌표는 레이어 사각형의 왼쪽 위 모서리를 기준으로 하며 레이어는 `origin=` 또는 해당 기본값을 기준으로 배치됩니다. 레이어 사각형 외부의 패스의 모든 영역은 투명하게 유지됩니다.

단색 또는 텍스트 레이어에 `size=`을(를) 지정하지 않으면 패스의 크기를 결정하는 범위 내에서 레이어가 자체 크기 조정으로 간주됩니다. `origin=`을(를) 지정하지 않으면 기본적으로 경로 좌표 공간의 (0,0)이 됩니다. 이 워크플로우 프로세스를 사용하면 레이어 0의 원점을 기준으로 경로 좌표를 효과적으로 지정할 수 있습니다.

>[!NOTE]
>
>`scale=`, `rotate=` 및 `anchor=` 명령은 자체 크기 조정 단색 레이어에 허용되지 않습니다.

`*`pathDefinition`*`에서는 값을 구분하기 위해 공백 대신 쉼표를 사용한다는 점을 제외하고 SVG `<path>` 요소의 `d=` 특성 값과 유사한 문자열을 사용할 수 있습니다. `*`pathDefinition`*`에는 하나 이상의 닫힌 루프 하위 경로가 포함될 수 있습니다.

`*`pathDefinition`*`에서는 다음 경로 명령이 지원됩니다.

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 명령</b> </th> 
   <th class="entry"> <b> 이름</b> </th> 
   <th class="entry"> <b> 설명</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> 절대 이동 </p> </td> 
   <td> <p> x,y에서 새 하위 경로를 시작합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> 상대 이동 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> 절대 줄 </p> </td> 
   <td> <p> 현재 위치에서 x,y로 선을 그립니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto 상대 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 절대 곡선화 </p> </td> 
   <td> <p> 현재 위치에서 x,y로 베지어 곡선을 그립니다. x1,y1은 곡선 시작 부분의 제어점이고 x2,y2는 곡선 끝 부분의 제어점입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 상대 곡선 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> 현재 서브패스를 직선으로 닫습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

대문자 명령은 좌표 값이 레이어 사각형의 왼쪽 위를 기준으로 절대 픽셀 위치에 있음을 나타냅니다. 픽셀 오프셋은 현재 위치를 기준으로 소문자 명령을 따릅니다.

&#39;m&#39; 또는 &#39;M&#39;은 항상 새 하위 경로를 시작합니다. 끝에 &#39;Z&#39; 또는 &#39;z&#39;가 지정되지 않은 경우 서브패스는 직선으로 자동으로 닫힙니다.

하위 경로가 상대 이동(&#39;m&#39;)으로 시작하면 다음 중 하나에 상대적입니다.

* &#39;z&#39; 또는 &#39;Z&#39;로 닫힌 경우 이전 하위 경로의 시작점.
* 명시적으로 닫히지 않은 경우 이전 하위 경로의 끝점입니다.
* 첫 번째 하위 경로인 경우 0,0.

## 속성 {#section-d4127db0dac54e3cbd44f7ea1e001960}

레이어 속성입니다. `layer=comp`인 경우 현재 레이어 또는 합성 이미지에 적용됩니다. 효과 레이어는 이를 무시합니다.

레이어 원본 이미지에 지정된 이름의 경로가 없거나 레이어 원본이 이미지가 아니면 한정자 `clipPathE=`이(가) 무시됩니다.

## 기본값 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

없음 - 레이어를 추가로 클리핑하지 않습니다.

## 참조 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
