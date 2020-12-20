---
description: 이름이 포함된 패스의 테두리 상자로 자를 수 있습니다. 이 자르기는 다시 이미지 크기를 변경합니다.
seo-description: 이름이 포함된 패스의 테두리 상자로 자를 수 있습니다. 이 자르기는 다시 이미지 크기를 변경합니다.
seo-title: cropPathE
solution: Experience Manager
title: cropPathE
topic: Scene7 Image Serving - Image Rendering API
uuid: 4689fd20-dfa0-47eb-8184-cd233f1ac088
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 2%

---


# cropPathE{#croppathe}

이름이 포함된 패스의 테두리 상자로 자를 수 있습니다. 이 자르기는 다시 이미지 크기를 변경합니다.

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>레이어 소스 이미지에 포함된 경로 이름(ASCII만 해당). </p> <p> <span class="codeph"><span class="varname"> 경로 </span></span> 이름은 레이어 소스 이미지에 포함된 경로의 이름입니다. 이미지 내용에 상대적인 정렬을 유지하기 위해 필요에 따라 경로가 자동으로 변형됩니다. 둘 이상의 <span class="codeph"><span class="varname"> pathName</span></span>을(를) 지정하면 서버가 각 경로의 경계 상자로 한 번에 하나씩 잘립니다. 소스 이미지에 없는 <span class="codeph"><span class="varname"> pathName</span></span>은 무시됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 속성 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

레이어 속성입니다. `layer=comp`인 경우 현재 레이어나 합성 이미지에 적용됩니다. 효과 레이어에서 무시됩니다.

`cropPathE=` 레이어 소스 이미지에 지정된 이름의 경로가 없거나 레이어 소스가 이미지가 아닌 경우에는 이 값이 무시됩니다.

## 기본값 {#section-d1986aa31af14767aeb1b4a57add67f4}

없음. 추가 자르기 작업이 필요 없습니다.

## 참조 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[자르기](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
