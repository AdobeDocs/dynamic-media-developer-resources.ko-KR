---
description: 구성 속성은 응답형 이미지 라이브러리에서 관리하는 IMG 요소에 직접 대한 속성으로 정의됩니다. 각 이미지에는 고유한 속성 세트가 있을 수 있습니다.
solution: Experience Manager
title: 명령 참조 - 구성 속성
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 1%

---

# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

구성 속성은 응답형 이미지 라이브러리에서 관리하는 IMG 요소에 직접 대한 속성으로 정의됩니다. 각 이미지에는 고유한 속성 세트가 있을 수 있습니다.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

선택적.

이미지 제공이 제공하는 이미지의 URL입니다. URL이 없으면 라이브러리는에 설정된 값을 사용합니다 `src` 속성을 폴백으로 지정합니다. 이 속성은 응답형 이미지 라이브러리가 다른 위치에서 관리하는 초기 이미지 및 동적 이미지를 제공합니다.

**예**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

If `data-src` 이(가) 설정되어 있습니다. `src` 는 선택 사항이며 추가할 모든 URL을 포함할 수 있습니다. 예를 들어 라이브러리가 사용하는 동일한 이미지 제공 기반 이미지에 대한 URL을 포함할 수 있습니다. 또는 시작 시 추가 서버 왕복 이동을 방지하기 위해 GIF 자리 표시자 또는 데이터 URI를 포함할 수 있습니다.

If `data-src` 이(가) 설정되지 않았습니다. `src` 는 필수 항목이며 이미지 제공에서 제공하는 이미지에 대한 URL을 포함해야 합니다.

**예**

에 데이터 URI 사용 `src` 속성 및 이미지 제공 URL `data-src` 특성:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## 데이터 중단점 {#section-3bf62a89ff3e40569848c1fe3ac7886c}

쉼표로 구분된 중단점 목록 및 선택적으로 뒤에 콜론( `:`)를 참조하고 이미지 제공 명령 또는 이미지 사전 설정을 참조하십시오. 각 중단점은 논리적 CSS 픽셀에서 정의된 이미지 너비 값입니다. 라이브러리는 목록에서 가장 가까운 값이 더 큰 이미지를 로드하고 런타임 CSS 이미지 폭과 일치하도록 클라이언트에서 축소합니다. 고밀도 화면에서 작업하는 경우 서버에서 로드되는 이미지 렌디션은 중단점 값에 디바이스의 픽셀 비율을 곱한 값을 나타냅니다.

목록의 중단점에 대해 하나 이상의 이미지 제공 명령 또는 이미지 사전 설정 이름을 정의할 수 있습니다. 이러한 추가 매개 변수는 이 특정 중단점이 현재 활성화된 경우에만 이미지에 적용됩니다.

다음과 같이 응답 이미지 크기에 영향을 주는 보기 명령을 제외하고 지원되는 모든 이미지 제공 명령을 사용할 수 있습니다 `wid=`, `hei=`, 또는 `scl=`. 이미지 사전 설정에도 동일한 제한 사항이 적용됩니다. 응답형 이미지 라이브러리와 함께 사용되는 이미지 사전 설정에는 이러한 명령이 없어야 합니다.

여러 이미지 제공 명령 또는 이미지 사전 설정 이름은 &quot; `&`&quot; 문자 이미지 제공 명령의 값에 쉼표가 있으면 해당 쉼표가 로 바뀝니다 `%2C`. 이미지 사전 설정 이름은 달러 기호( `$`).

**예제**

**중단점만 사용**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**이미지 제공 명령 사용**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**이미지 사전 설정 사용**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**이미지 사전 설정 및 이미지 제공 명령 사용**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## 데이터 모드 {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

AEM 6.4 이상 및 Dynamic Media Viewers 5.9 이상에서 다음 두 가지 스마트 자르기 모드를 사용할 수 있습니다.

* **수동** - 사용자 정의 중단점 및 해당 이미지 서비스 명령이 이미지 요소의 특성 내에 정의되어 있습니다.
* **스마트 자르기** - 계산된 스마트 자르기 렌디션은 게재 서버에서 자동으로 검색됩니다. 이미지 요소의 런타임 크기를 사용하여 최상의 렌디션을 선택합니다.

스마트 자르기 모드를 사용하려면 `data-mode` 특성 대상 `smart crop`.

**예**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

연결된 이미지 요소는 `s7responsiveViewer` 중단점이 변경될 때 런타임에 이벤트가 발생합니다.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
