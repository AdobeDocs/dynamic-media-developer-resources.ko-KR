---
title: setParams
description: 스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조입니다.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 65461c4b-efa3-41f5-9f90-e96d129981da
TQID: 'https://experienceleague.adobe.com/P0drvnRKomJsedVFiffSW4JmnhuiqQcs4AA3hsG3cZw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%
---
# setParams{#setparams}

스마트 자르기 비디오 뷰어에 대한 JavaScript API 참조입니다.

` setParams( *`매개 변수`*)`

하나 이상의 매개 변수를 지정된 값으로 설정합니다. 메서드 인수 구문은 URL 쿼리 문자열과 동일합니다. 즉, `&`(으)로 구분된 이름=값 쌍을 나타냅니다. 쿼리 문자열과 마찬가지로 이름 및 값은 UTF8을 사용하여 퍼센트 인코딩됩니다. `init()`을(를) 호출하기 전에 이 매개 변수를 호출해야 합니다.

뷰어 구성 정보가 `config` JSON 개체와 함께 생성자에 전달되는 경우 이 메서드는 선택 사항입니다.

[init](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)도 참조하세요.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 매개 변수</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> 이름=값 매개 변수 쌍은 <span class="codeph"> &amp;</span>(으)로 구분됩니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&SmartCropVideoPlayer.playback=progressive")
```
