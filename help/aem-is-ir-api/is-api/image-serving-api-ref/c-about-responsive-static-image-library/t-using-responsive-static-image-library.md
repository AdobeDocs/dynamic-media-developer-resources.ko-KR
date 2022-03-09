---
title: 응답형 이미지 라이브러리 사용
description: 웹 페이지에 응답형 이미지 라이브러리를 추가하고 라이브러리를 사용하여 기존 이미지를 관리하려면 다음 단계를 완료하십시오.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# 응답형 이미지 라이브러리 사용{#using-responsive-image-library}

웹 페이지에 응답형 이미지 라이브러리를 추가하고 라이브러리를 사용하여 기존 이미지를 관리하려면 다음 단계를 완료하십시오.

**응답형 이미지 라이브러리를 사용하려면**

1. Dynamic Media Classic에서, [이미지 사전 설정 만들기](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) 사전 설정에서 응답형 이미지 라이브러리를 사용할 계획입니다.

   응답형 이미지 라이브러리에 사용되는 이미지 사전 설정을 정의할 때는 이미지 크기에 영향을 주는 설정(예: )을 사용하지 마십시오 `wid=`, `hei=`, 또는 `scl=`. 이미지 사전 설정에서 크기 필드를 지정하지 마십시오. 대신 빈 값으로 둡니다.
1. 라이브러리 JavaScript 파일을 웹 페이지에 추가합니다.

   라이브러리 API를 사용하려면 먼저 다음을 포함해야 합니다 `responsive_image.js`. 이 JavaScript 파일은 `libs/` 표준 IS-Viewers 배포의 하위 폴더:

   `<s7viewers_root>/libs/responsive_image.js`
1. 기존 이미지를 설정합니다.

   라이브러리는 작업 중인 이미지 인스턴스에서 특정 구성 속성을 읽습니다. 다음 항목 앞에 속성을 정의합니다 `s7responsiveImage` 이러한 이미지에 대한 API 함수가 호출됩니다.

   기존 이미지 URL을 `data-src` 속성을 사용합니다. 그런 다음 기존 `src` 1x1 GIF 이미지를 데이터 URI로 인코딩할 속성입니다. 이렇게 하면 로드 시 웹 페이지에서 보내는 HTTP 요청 수가 줄어듭니다. 그러나 SEO(검색 엔진 최적화)가 필요한 경우 `title` 속성 을 포함합니다.

   다음은 정의 예입니다 `data-breakpoints` 이미지의 속성 및 데이터 URI로 인코딩된 1x1 GIF 사용:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. 호출 `s7responsiveImage` 라이브러리가 관리하는 모든 이미지 인스턴스에 대한 API 함수입니다.

   호출 `s7responsiveImage` 라이브러리가 관리하는 모든 이미지 인스턴스에 대한 API 함수입니다. 이러한 호출 후에 라이브러리는 원래 이미지를 의 런타임 크기에 따라 이미지 제공 기능에서 다운로드한 이미지로 바꿉니다 `IMG` 웹 페이지 레이아웃과 장치 화면의 밀도에 있는 요소입니다.

   다음 코드는 를 호출하는 예제입니다 `s7responsiveImage` 이미지의 API 함수에서 `responsiveImage` 는 해당 이미지의 ID입니다.

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 예 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

라이브러리는 웹 페이지에서 여러 이미지 인스턴스 작업을 동시에 지원합니다. 따라서 라이브러리를 관리할 각 이미지에 대해 위의 1단계와 2단계를 반복합니다.

이미지 요소를 유연하게 계산할 수 있도록 하는 것은 웹 페이지의 책임입니다. 응답형 이미지 라이브러리 자체에서는 고정 크기와 &quot;유동&quot; 이미지를 구분하지 않습니다. 고정 크기 이미지에 적용하면 새 이미지가 한 번만 로드됩니다.

다음 코드는 응답형 이미지 라이브러리에서 관리하는 단일 유체 이미지가 있는 간단한 웹 페이지의 전체 예입니다. 이 예에는 이미지를 웹 브라우저 창 크기에 &quot;응답형&quot;으로 만들기 위한 추가 CSS 스타일이 포함되어 있습니다.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**스마트 자르기 사용**

AEM 6.4 및 Dynamic Media Viewers 5.9에서 사용할 수 있는 두 가지 스마트 자르기 모드가 있습니다.

* **수동** - 사용자 정의 중단점 및 해당 이미지 서비스 명령은 이미지 요소의 속성 내에 정의됩니다.
* **스마트 자르기** - 계산된 스마트 자르기 렌디션은 게재 서버에서 자동으로 검색됩니다. 이미지 요소의 런타임 크기를 사용하여 최상의 렌디션을 선택합니다.

스마트 자르기 모드를 사용하려면 `data-mode` 속성 `smart crop`. For example:

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

연결된 이미지 요소는 `s7responsiveViewer` 중단점이 변경되는 경우 런타임 중에 발생합니다.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
