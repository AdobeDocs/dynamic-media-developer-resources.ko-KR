---
description: 레이어 클립 경로. 현재 레이어의 클립 경로를 지정합니다.
solution: Experience Manager
title: clipPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 1%

---

# clipPath{#clippath}

레이어 클립 경로. 현재 레이어의 클립 경로를 지정합니다.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

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

`clipPath=`에 의해 정의된 영역을 벗어나는 레이어의 모든 부분은 투명하게 렌더링됩니다.

`*``*` pathName은 레이어 소스 이미지에 포함된 경로의 이름입니다. 패스가 자동으로 변형되어 이미지 내용에 대한 상대적 맞춤을 유지합니다. 두 개 이상의 `*`pathName`*`을(를) 지정한 경우 서버는 이미지를 이러한 경로의 교차 지점으로 클립합니다. 소스 이미지에 없는 `*`pathName`*`은(는) 무시됩니다.

>[!NOTE]
>
>`*`pathName`*`에는 ASCII 문자열만 지원됩니다.

`*``*` pathDefinitioninstriction레이어 픽셀 좌표에서 명시적 경로 데이터를 지정할 수 있습니다.

`size=`이 지정되어 있고 0,0 이 아닌 경우 레이어의 크기가 미리 지정됩니다. 이 경우 경로 좌표는 레이어 사각형의 왼쪽 위 모서리를 기준으로 하며 레이어는 `origin=` 또는 그 기본값을 기준으로 배치됩니다. 레이어 사각형 바깥쪽에 있는 경로의 모든 영역은 투명하게 유지됩니다.

단색 또는 텍스트 레이어에 대해 `size=`을 지정하지 않으면 해당 레이어의 크기가 결정되는 패스의 범위에 따라 자체 크기가 고려됩니다. `origin=`을 지정하지 않으면 기본적으로 경로 좌표 공간의 (0,0)이 됩니다. 따라서 레이어 0의 원점을 기준으로 경로 좌표를 지정할 수 있습니다.

>[!NOTE]
>
>`scale=`단색 레이어 `rotate=`를 자체 크기 `anchor=` 로 지정하는 경우에는 , 및 명령을 사용할 수 없습니다.

`*``*` pathDefinitionis는 값을 구분하는 공백  `d=` 대신 쉼표를 사용한다는 점을 제외하고 SVG  `<path>` 요소의 속성 값과 유사한 문자열을 허용합니다. `*``*` pathDefinition에는 하나 이상의 닫힌 루프 하위 경로가 포함될 수 있습니다.

다음 경로 명령은 `*`pathDefinition`*`에서 지원됩니다.

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
   <td> <b> </b> <span class="varname"> Mx,y</span> </td> 
   <td> <p> 절대 거부권 </p> </td> 
   <td> <p> x,y에서 새 하위 경로를 시작합니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
   <td> <p> 상대적 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> 절대선 </p> </td> 
   <td> <p> 현재 위치에서 x,y로 선을 그립니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto 상대 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 절대적 거부권 </p> </td> 
   <td> <p> 현재 위치에서 x,y로 베지어 곡선을 그립니다. x1,y1은 커브의 시작 부분에 있는 제어점이고 x2, y2는 커브의 끝 부분에 있는 제어점입니다. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 상대적 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> |  <b>z</b> </td> 
   <td> <p> 닫기 경로 </p> </td> 
   <td> <p> 현재 하위 경로를 직선으로 닫습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

대문자 명령은 좌표 값이 절대 픽셀 위치(레이어 사각형의 왼쪽 위에 상대적)임을 나타냅니다. 픽셀 오프셋은 현재 위치에 대해 소문자 명령을 따릅니다.

&#39;m&#39; 또는 &#39;M&#39;은 항상 새 하위 경로를 시작합니다. 끝에 &#39;Z&#39; 또는 &#39;z&#39;가 지정되지 않은 경우 하위 경로는 자동으로 닫히고(직선으로),

하위 경로가 상대 모비토(&#39;m&#39;)로 시작하는 경우 다음 중 하나에 상대적입니다.

* 이전 하위 경로가 &#39;z&#39; 또는 &#39;Z&#39;로 닫힌 경우 시작 지점입니다.
* 이전 하위 경로의 끝점이 명시적으로 닫히지 않은 경우 끝점입니다.
* 0,0. 첫 번째 하위 경로인 경우

## 속성 {#section-d4127db0dac54e3cbd44f7ea1e001960}

레이어 속성입니다. `layer=comp` 인 경우 현재 레이어 또는 복합 이미지에 적용됩니다. 효과 레이어가 이를 무시합니다.

`clipPathE=` 레이어 소스 이미지에서 지정된 이름의 경로를 찾을 수 없거나 레이어 소스가 이미지가 아닌 경우에는 이 무시됩니다.

## 기본값 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

없음, 레이어의 추가 클리핑이 없습니다.

## 참조 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
