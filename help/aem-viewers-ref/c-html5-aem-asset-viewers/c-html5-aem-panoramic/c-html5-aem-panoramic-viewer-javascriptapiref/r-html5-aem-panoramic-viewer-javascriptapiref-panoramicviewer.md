---
title: PanoramicViewer
description: 생성자, HTML5 Panoramic Viewer 인스턴스를 만듭니다.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
autotag-review: '2026-05-13T22:09:54.686Z'
TQID: 'https://experienceleague.adobe.com/zSYqLmLn-LQhkIIrPe31JIouevTWijICBcrmY3fol1M'
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
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%
---
# PanoramicViewer{#panoramicviewer}

`PanoramicViewer([config])`
생성자, HTML5 Panoramic Viewer 인스턴스를 만듭니다.

## 매개 변수 {#section-fa807db629ce43bab286b1e1dc96c492}

config
선택적 JSON 구성 개체 {Object}을(를) 사용하면 모든 뷰어 설정을 생성자에 전달하고 개별 setter 메서드를 호출하지 않을 수 있습니다. 여기에는 다음 속성이 포함됩니다.

* containerId - 뷰어가 삽입되는 DOM 컨테이너(일반적으로 DIV)의 {String} ID. 이 메서드가 호출될 때 컨테이너 요소를 만들 필요는 없지만 init()가 실행될 때 컨테이너가 있어야 합니다. 필수
* params - {Object} JSON 개체와 뷰어 구성 매개 변수가 함께 사용됩니다. 여기서 속성 이름은 뷰어별 구성 옵션 또는 SDK 수정자이고 해당 속성 값은 해당 설정 값입니다. 필수
* 처리기 - 뷰어 이벤트 콜백이 있는 {Object} JSON 개체입니다. 여기서 속성 이름은 지원되는 뷰어 이벤트 이름이고 속성 값은 적절한 콜백에 대한 JavaScript 함수 참조입니다. 뷰어 이벤트에 대한 자세한 내용은 이벤트 콜백 섹션을 참조하십시오. 선택적.


## 반환 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

없음.

## 예 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```
