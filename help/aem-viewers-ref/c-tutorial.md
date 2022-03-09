---
title: Viewer SDK 자습서
description: Viewer SDK는 사용자 지정 뷰어 개발을 위한 JavaScript 기반 구성 요소 집합을 제공합니다. 뷰어는 Adobe Dynamic Media에서 제공하는 리치 미디어 컨텐츠를 웹 페이지에 포함할 수 있는 웹 기반 애플리케이션입니다.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Viewer SDK 자습서{#viewer-sdk-tutorial}

Viewer SDK는 사용자 지정 뷰어 개발을 위한 JavaScript 기반 구성 요소 집합을 제공합니다. 뷰어는 Adobe Dynamic Media에서 제공하는 리치 미디어 컨텐츠를 웹 페이지에 포함할 수 있는 웹 기반 애플리케이션입니다.

예를 들어 SDK는 대화형 확대/축소 및 패닝 기능을 제공합니다. 또한 Dynamic Media Classic라는 백엔드 애플리케이션을 통해 Dynamic Media에 업로드된 자산의 360° 보기 및 비디오 재생을 제공합니다.

구성 요소는 HTML5 기능을 사용하더라도 Android™ 및 Apple iOS 장치, Internet Explorer 이상을 비롯한 데스크톱에서 작동하도록 디자인되었습니다. 이러한 종류의 경험은 지원되는 모든 플랫폼에 단일 워크플로우를 제공할 수 있음을 의미합니다.

SDK는 뷰어 컨텐츠를 구성하는 UI 구성 요소로 구성됩니다. CSS와 설정 정의 가져오기 및 구문 분석 또는 추적과 같은 일부 지원 역할이 있는 비UI 구성 요소를 통해 이러한 구성 요소의 스타일을 지정할 수 있습니다. 모든 구성 요소 동작은 다음과 같이 다양한 방법으로 지정할 수 있는 수정자를 통해 사용자 지정할 수 있습니다 `name=value` 쌍을 URL에 추가합니다.

이 자습서에는 기본 확대/축소 뷰어를 만드는 데 도움이 되는 다음 작업 순서가 포함되어 있습니다.

* [Adobe Developer Connection에서 최신 Viewer SDK를 다운로드합니다](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [뷰어 SDK 로드](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [뷰어에 스타일 추가](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [컨테이너 및 ZoomView 포함](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [뷰어에 MediaSet 및 색상 견본 구성 요소 추가](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [뷰어에 단추 추가](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [세로 색상 견본 구성](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Adobe Developer Connection에서 최신 Viewer SDK를 다운로드합니다 {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Adobe Developer Connection에서 최신 Viewer SDK를 다운로드합니다 <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->.

   >[!NOTE]
   >
   >SDK가 원격으로 로드되므로 Viewer SDK 패키지를 다운로드하지 않고도 이 자습서를 완료할 수 있습니다. 그러나 뷰어 패키지에는 사용자의 뷰어를 만드는 데 도움이 되는 추가 예와 API 참조 안내서가 포함되어 있습니다.

## 뷰어 SDK 로드 {#section-98596c276faf4cf79ccf558a9f4432c6}

1. 먼저 만들려는 기본 확대/축소 뷰어를 개발하기 위해 새 페이지를 설정합니다.

   빈 SDK 애플리케이션을 설정하는 데 사용하는 코드, Bootstrap 또는 로더에 있는 이 새 페이지를 고려해 보십시오. 즐겨찾는 텍스트 편집기를 열고 다음 HTML 마크업을 페이지에 붙여 넣습니다.

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
       <head> 
           <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> 
           <meta name="viewport" content="user-scalable=no, height=device-height, width=device-width, initial-scale=1.0, maximum-scale=1.0"/> 
   
           <!-- Hiding the Safari on iPhone OS UI components --> 
           <meta name="apple-mobile-web-app-capable" content="yes"/> 
           <meta name="apple-mobile-web-app-status-bar-style" content="black"/> 
           <meta name="apple-touch-fullscreen" content="no"/> 
   
           <title>Custom Viewer</title> 
   
           <!-- 
               Include Utils.js before you use any of the SDK components. This file  
               contains SDK utilities and global functions that are used to initialize the viewer and load viewer  
               components. The path to the Utils.js determines which version of the SDK that the viewer uses. You  
               can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Dynamic Media servers that have the SDK  
               installed.  
           --> 
           <script language="javascript" type="text/javascript"      
                   src="http://s7d1.scene7.com/s7sdk/2.8/js/s7sdk/utils/Utils.js"></script> 
   
       </head> 
       <body> 
           <script language="javascript" type="text/javascript"> 
           </script>  
       </body> 
   </html>
   ```

   다음 JavaScript 코드를 `script` 태그로 초기화되도록 `ParameterManager`. 이렇게 하면 내에서 SDK 구성 요소를 만들고 인스턴스화할 준비를 하는 데 도움이 됩니다 `initViewer` 함수:

   ```javascript {.line-numbers}
   /* We create a self-running anonymous function to encapsulate variable scope. Placing code inside such 
      a function is optional, but this prevents variables from polluting the global object.  */ 
   (function () { 
   
       // Initialize the SDK   
       s7sdk.Util.init(); 
   
       /* Create an instance of the ParameterManager component to collect components' configuration 
          that can come from a viewer preset, URL, or the HTML page itself. The ParameterManager  
          component also sends a notification s7sdk.Event.SDK_READY when all needed files are loaded 
          and the configuration parameters are processed. The other components should never be initialized 
          outside this handler. After defining the handler for the s7sdk.Event.SDK_READY event, it 
          is safe to initiate configuration initialization by calling ParameterManager.init(). */ 
       var params = new s7sdk.ParameterManager(); 
   
       /* Event handler for s7sdk.Event.SDK_READY dispatched by ParameterManager to initialize various components of  
          this viewer. */ 
       function initViewer() { 
   
       }  
   
       /* Add event handler for the s7sdk.Event.SDK_READY event dispatched by the ParameterManager when all modifiers 
          are processed and it is safe to initialize the viewer. */ 
       params.addEventListener(s7sdk.Event.SDK_READY, initViewer, false); 
   
       /* Initiate configuration initialization of ParameterManager. */ 
       params.init(); 
   
   }());
   ```

1. 파일을 빈 템플릿으로 저장합니다. 원하는 파일 이름을 사용할 수 있습니다.

   나중에 뷰어를 만들 때 이 빈 템플릿 파일을 참조로 사용합니다. 이 템플릿은 로컬에서, 웹 서버에서 제공될 때 작동합니다.

이제 뷰어에 스타일을 추가합니다.

## 뷰어에 스타일 추가 {#section-3783125360a1425eae5a5a334867cc32}

1. 만드는 이 전체 페이지 뷰어의 경우 몇 가지 기본 스타일을 추가할 수 있습니다.

   다음을 추가합니다 `style` 블록 `head`:

   ```html {.line-numbers}
   <style> 
       html, body { 
           width: 100%; 
           height: 100%; 
       } 
       body { 
           /* Remove any padding and margin around the edges of the browser window */ 
           padding: 0; 
           margin: 0; 
   
           /* We set overflow to hidden so that scroll bars do not flicker when resizing the window */ 
           overflow: hidden; 
       } 
   </style>
   ```

이제 구성 요소를 포함합니다 `Container` 및 `ZoomView`.

## 컨테이너 및 ZoomView 포함 {#section-1a01730663154a508b88cc40c6f35539}

1. 구성 요소를 포함하여 실제 뷰어를 만듭니다 `Container` 및 `ZoomView`.

   다음을 삽입합니다. `include` 아래쪽의 문 `<head>` 요소 - 뒤에 [!DNL Utils.js] 스크립트가 로드됨:

   ```javascript {.line-numbers}
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. 이제 다양한 SDK 구성 요소를 참조할 변수를 만듭니다.

   바로 위에 있는 기본 익명 함수의 맨 위에 다음 변수를 추가합니다 `s7sdk.Util.init()`:

   ```javascript {.line-numbers}
   var container, zoomView;
   ```

1. 다음 내용을 `initViewer` 함수를 사용하여 일부 한정자를 정의하고 각 구성 요소를 인스턴스화할 수 있습니다.

   ```javascript {.line-numbers}
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. 위의 코드가 제대로 실행되려면 `containerResize` 이벤트 처리기 및 도우미 함수:

   ```javascript {.line-numbers}
   /* Event handler for s7sdk.event.ResizeEvent.COMPONENT_RESIZE events dispatched by Container to resize 
      various view components included in this viewer. */ 
   function containerResize(event) { 
       resizeViewer(event.s7event.w, event.s7event.h); 
   } 
   
   /* Resize viewer components */ 
   function resizeViewer(width, height) { 
       zoomView.resize(width, height); 
   }
   ```

1. 만든 항목을 볼 수 있도록 페이지를 미리 봅니다. 페이지 모습은 다음과 같습니다.

   ![뷰어 예제 1개 이미지](assets/viewer-1.jpg)

이제 구성 요소를 추가합니다 `MediaSet` 및 `Swatches` 참조하십시오.

## 뷰어에 MediaSet 및 색상 견본 구성 요소 추가 {#section-02b8c21dd842400e83eae2a48ec265b7}

1. 사용자에게 세트에서 이미지를 선택할 수 있는 기능을 제공하기 위해 구성 요소를 추가할 수 있습니다 `MediaSet` 및 `Swatches`.

   다음 SDK를 추가하면 다음이 포함됩니다.

   ```javascript {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. 변수 목록을 다음과 같이 업데이트합니다.

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches;
   ```

1. 인스턴스화 `MediaSet` 및 `Swatches` 내의 구성 요소 `initViewer` 함수 위에 있어야 합니다.

   를 인스턴스화하십시오 `Swatches` 인스턴스 뒤 `ZoomView` 및 `Container` 구성 요소를 제외한 스택 순서는 `Swatches`:

   ```javascript {.line-numbers}
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. 이제 다음 이벤트 처리기 함수를 추가합니다.

   ```javascript {.line-numbers}
   /* Event handler for the s7sdk.event.AssetEvent.NOTF_SET_PARSED event dispatched by MediaSet to 
      assign the asset to the Swatches when parsing is complete. */ 
   function onSetParsed(e) { 
   
       // set media set for Swatches to display  
       var mediasetDesc = e.s7event.asset;  
       swatches.setMediaSet(mediasetDesc); 
   
       // select the first swatch by default  
       swatches.selectSwatch(0, true);      
   } 
   
   /* Event handler for s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT events dispatched by Swatches to switch 
      the image in the ZoomView when a different swatch is selected. */ 
   function swatchSelected(event) {     
       zoomView.setItem(event.s7event.asset);  
   }
   ```

1. 다음 CSS를 뷰어에 추가하여 색상 견본을 뷰어 하단에 배치합니다. `style` 요소:

   ```CSS {.line-numbers}
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. 뷰어를 미리 봅니다.

   색상 견본은 뷰어 왼쪽 아래에 있습니다. 색상 견본이 전체 뷰어 너비를 갖도록 하려면 사용자가 브라우저 크기를 조정할 때마다 색상 견본의 크기를 수동으로 조정하도록 호출을 추가합니다. 다음 내용을 `resizeViewer` 함수:

   ```javascript {.line-numbers}
   swatches.resize(width, swatches.getHeight());
   ```

   이제 뷰어가 다음 이미지와 같습니다. 뷰어의 브라우저 창 크기를 조정하고 결과 동작을 확인합니다.

   ![뷰어 예제 2 이미지](assets/viewer-2.jpg)

이제 뷰어에 확대, 축소 및 확대/축소 재설정 단추를 추가합니다.

## 뷰어에 단추 추가 {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. 현재 사용자는 클릭 또는 터치 제스처만 사용하여 확대/축소할 수 있습니다. 따라서 뷰어에 몇 가지 기본 확대/축소 컨트롤 단추를 추가합니다.

   다음 단추 구성 요소를 추가합니다.

   ```CSS {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. 변수 목록을 다음과 같이 업데이트합니다.

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. 단추 인스턴스화 `initViewer` 함수 위에 있어야 합니다.

   순서를 지정하지 않는 한 순서가 중요하다는 것을 기억하십시오 `z-index` CSS에서:

   ```CSS {.line-numbers}
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. 이제 단추에 다음을 추가하여 단추의 몇 가지 기본 스타일을 정의합니다 `style` 파일의 맨 위에 있는 블록:

   ```CSS {.line-numbers}
   /* define styles common to all button components and their sub-classes */ 
   .s7button { 
       position:absolute; 
       width: 28px; 
       height: 28px; 
       z-index:100; 
   } 
   
   /* position individual buttons*/ 
   .s7zoominbutton  { 
       top: 50px; 
       left: 50px; 
    } 
   .s7zoomoutbutton  { 
       top: 50px; 
       left: 80px; 
    } 
   .s7zoomresetbutton  { 
       top: 50px; 
       left: 110px; 
    }
   ```

1. 뷰어를 미리 봅니다. 다음과 같이 표시됩니다.

   ![뷰어 예제 3 이미지](assets/viewer-3.jpg)

   이제 오른쪽에 세로로 정렬되도록 색상 견본을 구성합니다.

## 세로 색상 견본 구성 {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. 수정자를 `ParameterManager` 인스턴스.

   의 맨 위에 다음 내용을 추가합니다 `initViewer` 함수를 사용하여 `Swatches` 축소판 레이아웃을 단일 행으로 표시:

   ```javascript {.line-numbers}
   params.push("Swatches.tmblayout", "1,0");
   ```

1. 내에서 다음 크기 조정 호출을 업데이트합니다 `resizeViewer`:

   ```javascript {.line-numbers}
   swatches.resize(swatches.getWidth(), height);
   ```

1. 다음을 편집합니다 `s7swatches` 규칙 `ZoomViewer.css`:

   ```CSS {.line-numbers}
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. 뷰어를 미리 봅니다. 다음과 같습니다.

   ![뷰어 예 4 이미지](assets/viewer-4.jpg)

   이제 기본 확대/축소 뷰어가 완료되었습니다.

   이 뷰어 튜토리얼에서는 Dynamic Media Viewer SDK에서 제공하는 사항의 기본 사항을 다룹니다. SDK를 사용하여 작업할 때 다양한 표준 구성 요소를 사용하여 타겟 대상에 대한 풍부한 보기 경험을 쉽게 작성하고 스타일을 지정할 수 있습니다.
