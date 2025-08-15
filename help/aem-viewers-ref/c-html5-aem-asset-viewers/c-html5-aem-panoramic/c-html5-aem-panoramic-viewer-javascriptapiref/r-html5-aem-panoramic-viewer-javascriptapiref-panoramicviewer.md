---
title: PanoramicViewer
description: 생성자, HTML5 Panoramic Viewer 인스턴스를 만듭니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 3%

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
