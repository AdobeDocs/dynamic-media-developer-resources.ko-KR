---
description: 구성 속성은 응답형 이미지 라이브러리가 관리하는 IMG 요소에 직접 속성으로 정의됩니다. 각 이미지에는 고유한 특성 세트가 있을 수 있습니다.
solution: Experience Manager
title: 명령 참조 - 구성 속성
feature: Dynamic Media Classic,SDK/API
role: 개발자,비즈니스 전문가
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# 명령 참조 - 구성 특성{#command-reference-configuration-attributes}

구성 속성은 응답형 이미지 라이브러리가 관리하는 IMG 요소에 직접 속성으로 정의됩니다. 각 이미지에는 고유한 특성 세트가 있을 수 있습니다.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

선택 사항입니다.

이미지 제공에서 제공하는 이미지의 URL. URL이 없으면 라이브러리는 `src` 속성에 설정된 값을 폴백으로 사용합니다. 이 속성은 반응형 이미지 라이브러리가 다른 위치에서 관리하는 초기 이미지와 동적 이미지를 제공합니다.

**예**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

`data-src`이(가) 설정된 경우 `src`은 선택 사항이며 추가할 URL을 포함할 수 있습니다. 예를 들어 라이브러리에서 사용하는 동일한 이미지 제공 기반 이미지에 대한 URL을 포함할 수 있습니다. 또는 GIF 자리 표시자를 포함하거나 데이터 URI를 포함시켜 시작할 때 추가 서버 라운드트립을 방지할 수 있습니다.

`data-src`이(가) 설정되어 있지 않으면 `src`은 필수 항목이며 이미지 제공 시 제공하는 이미지에 대한 URL을 포함해야 합니다.

**예**

`src` 속성에 대한 데이터 URI와 `data-src` 속성에 대한 이미지 제공 URL 사용:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## 데이터 중단점 {#section-3bf62a89ff3e40569848c1fe3ac7886c}

쉼표로 구분된 중단점 목록이며, 원할 경우 콜론( `:`) 및 이미지 제공 명령 또는 이미지 사전 설정이 뒤따릅니다. 각 중단점은 논리적 CSS 픽셀에 정의된 이미지 너비 값입니다. 라이브러리는 목록에서 가장 큰 값으로 이미지를 로드하고 런타임 CSS 이미지 폭에 맞게 클라이언트에서 크기를 축소합니다. 고밀도 화면에서 작업하는 경우 서버에서 로드된 이미지 표현물은 중단점 값을 장치의 픽셀 비율에 곱하는 값을 나타냅니다.

목록의 중단점에 대해 하나 이상의 이미지 제공 명령 또는 이미지 사전 설정 이름을 정의할 수 있습니다. 이러한 추가 매개 변수는 이 특정 중단점이 현재 활성 상태일 경우에 이미지만 적용됩니다.

`wid=`, `hei=` 또는 `scl=`와 같이 응답 이미지 크기에 영향을 주는 보기 명령을 제외하고 지원되는 모든 이미지 제공 명령을 사용할 수 있습니다. 동일한 제한이 이미지 사전 설정에 적용됩니다.응답형 이미지 라이브러리에 사용된 이미지 사전 설정에는 이러한 명령이 포함되어 있지 않아야 합니다.

여러 이미지 제공 명령 또는 이미지 사전 설정 이름은 &quot; `&`&quot; 문자로 구분됩니다. 이미지 제공 명령에 쉼표가 있는 경우, 이러한 쉼표는 `%2C`로 대체됩니다. 이미지 사전 설정 이름은 달러 기호( `$`)로 래핑됩니다.

**예제**

**중단점만 사용**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**이미지 제공 명령 사용**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**이미지 사전 설정 사용**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**이미지 사전 설정 및 이미지 제공 명령 사용**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

다음의 두 가지 스마트 자르기 모드는 AEM 6.4 이상 및 Dynamic Media Viewers 5.9 이상에서 사용할 수 있습니다.

* **사용자**  정의 중단점 및 해당 이미지 서비스 명령은 이미지 요소의 특성 내에 정의됩니다.
* **스마트 자르기**  - 계산된 스마트 자르기 변환은 배달 서버에서 자동으로 검색됩니다. 이미지 요소의 런타임 크기를 사용하여 최상의 변환이 선택됩니다.

스마트 자르기 모드를 사용하려면 `data-mode` 속성을 `smart crop`로 설정합니다.

**예**

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

연결된 이미지 요소는 중단점이 변경될 때 런타임 중에 `s7responsiveViewer` 이벤트를 전달합니다.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```

