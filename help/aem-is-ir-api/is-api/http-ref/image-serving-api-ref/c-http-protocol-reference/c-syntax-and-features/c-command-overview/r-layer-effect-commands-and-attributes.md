---
description: 이러한 명령을 사용하여 그림자 효과나 광선 효과와 같은 레이어 효과를 정의할 수 있습니다. 효과 레이어는 다른 모든 명령을 무시합니다.
seo-description: 이러한 명령을 사용하여 그림자 효과나 광선 효과와 같은 레이어 효과를 정의할 수 있습니다. 효과 레이어는 다른 모든 명령을 무시합니다.
seo-title: 레이어 효과 명령
solution: Experience Manager
title: 레이어 효과 명령
topic: Scene7 Image Serving - Image Rendering API
uuid: 5fef90d1-0507-497b-9187-869672996852
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 레이어 효과 명령{#layer-effect-commands}

이러한 명령을 사용하여 그림자 효과나 광선 효과와 같은 레이어 효과를 정의할 수 있습니다. 효과 레이어는 다른 모든 명령을 무시합니다.

<table id="simpletable_3094B9783772437FAACF9B382F7A32EE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> blendMode</a> </p></td> 
  <td class="stentry"> <p>레이어 혼합 모드를 지정합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> color</a> </p></td> 
  <td class="stentry"> <p>주 효과 색상 및 불투명도를 지정합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135" type="reference" format="dita" scope="local"> 효과</a> </p></td> 
  <td class="stentry"> <p>효과 레이어 세그먼트를 시작하고 z 순서를 지정합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464" type="reference" format="dita" scope="local"> maskUse</a> </p></td> 
  <td class="stentry"> <p>부모의 레이어 마스크(알파 채널)를 사용하는 방법을 지정합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-blur.md#reference-00638f29e59b49c99f6bba27daf24668" type="reference" format="dita" scope="local"> op_blur</a> </p></td> 
  <td class="stentry"> <p>효과를 페더링합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a" type="reference" format="dita" scope="local"> op_grow</a> </p></td> 
  <td class="stentry"> <p>레이어 효과를 확대하거나 축소합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-noise.md#reference-763c4a890fe24bb6bb5ae9dad4e2da94" type="reference" format="dita" scope="local"> op_noise</a> </p></td> 
  <td class="stentry"> <p>효과에 노이즈를 추가합니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opac</a> </p></td> 
  <td class="stentry"> <p>레이어 불투명도를 줄입니다. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> pos</a> </p></td> 
  <td class="stentry"> <p>효과 레이어를 상위 레이어를 기준으로 배치합니다. </p></td> 
 </tr> 
</table>
