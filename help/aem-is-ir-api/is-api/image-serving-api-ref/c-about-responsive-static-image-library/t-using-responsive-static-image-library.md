---
description: 웹 페이지에 응답형 이미지 라이브러리를 추가하고 라이브러리를 사용하여 기존 이미지를 관리하려면 다음 단계를 완료하십시오.
solution: Experience Manager
title: 반응형 이미지 라이브러리 사용
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 0%

---


# 반응형 이미지 라이브러리 사용{#using-responsive-image-library}

웹 페이지에 응답형 이미지 라이브러리를 추가하고 라이브러리를 사용하여 기존 이미지를 관리하려면 다음 단계를 완료하십시오.

**반응형 이미지 라이브러리를 사용하려면**

1. 사전 설정과 함께 응답형 이미지 라이브러리를 사용할 계획이면 SPS에서 [이미지 사전 설정](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html)을 만듭니다.

   응답형 이미지 라이브러리에 사용되는 이미지 사전 설정을 정의할 때 `wid=`, `hei=` 또는 `scl=` 등의 이미지 크기에 영향을 주는 설정을 사용하지 마십시오. 이미지 사전 설정에서 크기 필드를 지정하지 마십시오. 대신 빈 값으로 두십시오.
1. 웹 페이지에 라이브러리 JavaScript 파일을 추가합니다.

   라이브러리 API를 사용하려면 먼저 `responsive_image.js`을(를) 포함해야 합니다. 이 JavaScript 파일은 표준 IS-뷰어 배포의 `libs/` 하위 폴더에 있습니다.

   `<s7viewers_root>/libs/responsive_image.js`
1. 기존 이미지를 설정합니다.

   라이브러리는 작업 중인 이미지 인스턴스에서 특정 구성 속성을 읽습니다. 해당 이미지에 대해 `s7responsiveImage` API 함수가 호출되기 전에 특성을 정의합니다.

   기존 이미지 URL을 `data-src` 속성에 배치하는 것도 좋습니다. 그런 다음 기존 `src` 속성을 설정하여 1x1 GIF 이미지를 데이터 URI로 인코딩합니다. 이렇게 하면 로드 시 웹 페이지가 보내는 HTTP 요청 수가 줄어듭니다. 그러나 SEO(검색 엔진 최적화)가 필요한 경우 이미지 인스턴스에 `title` 속성을 설정하는 것이 좋습니다.

   다음은 이미지에 대해 `data-breakpoints` 속성을 정의하고 데이터 URI로 인코딩된 1x1 GIF를 사용하는 예입니다.

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. 라이브러리가 관리하는 모든 이미지 인스턴스에 대해 `s7responsiveImage` API 함수를 호출합니다.

   라이브러리가 관리하는 모든 이미지 인스턴스에 대해 `s7responsiveImage` API 함수를 호출합니다. 이러한 호출 후에 라이브러리는 웹 페이지 레이아웃의 `IMG` 요소 런타임 크기 및 장치 화면의 밀도에 따라 이미지 제공 기능에서 다운로드한 이미지로 원본 이미지를 대체합니다.

   다음 코드는 `responsiveImage`이(가) 해당 이미지의 ID라고 가정하고 이미지에서 `s7responsiveImage` API 함수를 호출하는 예입니다.

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 예 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

라이브러리는 웹 페이지에서 동시에 많은 이미지 인스턴스를 사용하여 작업할 수 있도록 지원합니다. 따라서 라이브러리를 관리할 각 이미지에 대해 위의 1단계와 2단계를 반복합니다.

이미지 요소의 스타일을 지정하여 크기를 유연하게 만드는 것은 웹 페이지의 책임입니다. 반응형 이미지 라이브러리 자체는 고정된 크기와 &quot;유동&quot; 이미지를 구별하지 않습니다. 고정 크기의 이미지에 적용하면 새 이미지가 한 번만 로드됩니다.

다음 코드는 응답형 이미지 라이브러리에서 관리되는 단일 유동 이미지가 있는 간단한 웹 페이지의 완전한 예입니다. 이 예에는 웹 브라우저 창 크기에 &quot;반응형&quot; 이미지를 만들기 위한 추가 CSS 스타일이 포함되어 있습니다.

```
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

AEM 6.4 및 Dynamic Media Viewers 5.9에서는 두 가지 스마트 자르기 모드를 사용할 수 있습니다.

* **사용자**  정의 중단점 및 해당 이미지 서비스 명령은 이미지 요소의 특성 내에 정의됩니다.
* **스마트 자르기**  - 계산된 스마트 자르기 변환은 배달 서버에서 자동으로 검색됩니다. 이미지 요소의 런타임 크기를 사용하여 최상의 변환이 선택됩니다.

스마트 자르기 모드를 사용하려면 `data-mode` 속성을 `smart crop`로 설정합니다. 예:

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
