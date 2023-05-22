---
title: 인라인 확대/축소 뷰어 사용자 지정
description: 인라인 확대/축소 뷰어 사용자 지정
keywords: 반응형
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 8818bee3-dcdb-4a36-bddb-14dd10d0ea52
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 0%

---

# 인라인 확대/축소 뷰어 사용자 지정{#customizing-inline-zoom-viewer}

모든 시각적 사용자 지정 및 대부분의 비헤이비어 사용자 지정은 사용자 지정 CSS를 만들어 수행합니다.

제안된 워크플로우는 적절한 뷰어에 대한 기본 CSS 파일을 가져와서 다른 위치에 복사하고, 사용자 지정하고, 에서 사용자 지정된 파일의 위치를 지정하는 것입니다. `style=` 명령입니다.

기본 CSS 파일은 다음 위치에서 찾을 수 있습니다.

`<s7_viewers_root>/html5/InlineZoomViewer.css`

사용자 지정 CSS 파일은 기본 클래스 선언과 동일한 클래스 선언을 포함해야 합니다. 클래스 선언을 생략하면 뷰어가 사용자 인터페이스 요소에 기본 스타일을 제공하지 않으므로 제대로 작동하지 않습니다.

또한 인라인 확대/축소 기능에 필요하므로 기본 뷰어 CSS에서 다음 CSS 선언을 유지하는 것이 중요합니다.

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 width: 100%; 
 height: 100%; 
 left: 0; 
 top: 0; 
 border: none; 
 z-index:999; 
}
```

사용자 지정 CSS 규칙을 제공하는 또 다른 방법은 웹 페이지에서 직접 또는 연결된 외부 CSS 규칙 중 하나에 포함된 스타일을 사용하는 것입니다.

사용자 지정 CSS를 만들 때는 뷰어가 `.s7flyoutviewer` 클래스를 컨테이너 DOM 요소에 추가합니다. 로 전달된 외부 CSS 파일을 사용하는 경우 `style=` 명령, 사용 `.s7flyoutviewer` 클래스를 CSS 규칙에 대한 하위 항목 선택기의 상위 클래스로 사용합니다. 웹 페이지에서 임베드된 스타일을 수행하는 경우 다음과 같이 이 선택기에 컨테이너 DOM 요소의 ID도 부여합니다.

`#<containerId>.s7flyoutviewer`

## 응답형 디자인 CSS 구축 {#section-c1e74f5114ad418884ca1c95f5ea5b63}

사용자의 장치 또는 특정 웹 페이지 레이아웃에 따라 컨텐츠를 다르게 표시하도록 다양한 장치와 CSS의 포함 크기를 타깃팅할 수 있습니다. 이 기능에는 다양한 웹 페이지 레이아웃, 사용자 인터페이스 요소 크기 및 아트워크 해상도가 포함되지만 이에 국한되지 않습니다.

뷰어는 반응형 디자인 CSS를 만드는 두 가지 방법인 CSS 마커 및 표준 CSS 미디어 쿼리를 지원합니다. 이러한 메서드는 독립적으로 사용하거나 함께 사용할 수 있습니다.

**CSS 마커**

응답형 디자인 CSS를 만드는 데 도움이 되도록 뷰어는 최상위 뷰어 컨테이너 요소에 동적으로 할당되는 특수 CSS 클래스인 CSS 마커를 지원합니다. 할당은 런타임 뷰어 크기와 현재 장치에서 사용되는 입력 유형을 기반으로 합니다.

CSS 마커의 첫 번째 그룹은 `.s7size_large`, `.s7size_medium`, 및 `.s7size_small` 클래스입니다. 뷰어 컨테이너의 런타임 영역을 기반으로 적용됩니다. 즉, 뷰어 영역이 일반적인 데스크톱 모니터의 크기 이상인 경우 `.s7size_large` 영역의 크기가 일반적인 태블릿 장치에 가까운 경우 사용됩니다. `.s7size_medium` 이(가) 할당되었습니다. 휴대폰 화면과 유사한 영역의 경우, `.s7size_small` 이(가) 설정되어 있습니다. 이러한 CSS 마커의 주요 목적은 다양한 화면과 뷰어 크기에 대해 다양한 사용자 인터페이스 레이아웃을 만드는 것입니다.

CSS 마커의 두 번째 그룹은 `.s7mouseinput` 및 `.s7touchinput`. 마커 `.s7touchinput` 는 현재 장치에 터치 입력 기능이 있는 경우 설정됩니다. 그렇지 않으면 `.s7mouseinput` 를 사용합니다. 이러한 마커는 일반적으로 터치 입력에 더 큰 요소가 필요하기 때문에 다양한 입력 유형에 대해 다양한 화면 크기를 갖는 사용자 인터페이스 입력 요소를 만들기 위한 것입니다. 장치에 마우스 입력 기능과 터치 기능이 모두 있는 경우 `.s7touchinput` 가 설정되고 뷰어가 터치 친화적인 사용자 인터페이스를 렌더링합니다.

다음 샘플 CSS는 마우스 입력이 있는 시스템의 경우 확대 단추 크기를 28 x 28픽셀로 설정하고 터치 디바이스의 경우 56 x 56픽셀로 설정합니다. 또한 뷰어 크기가 작아지는 경우 버튼을 완전히 숨깁니다.

```
.s7flyoutviewer.s7mouseinput .s7swatches .s7thumb {  
 width: 28px; 
 height: 28px; 
} 
.s7flyoutviewer.s7touchinput .s7swatches .s7thumb {  
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer.s7size_small .s7swatches {  
 visibility: hidden; 
}
```

픽셀 밀도가 다른 장치를 타깃팅하려면 CSS 미디어 쿼리를 사용하십시오. 다음 미디어 쿼리 블록에는 고밀도 화면에만 해당하는 CSS가 포함되어 있습니다.

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS 마커를 사용하는 것은 반응형 디자인 CSS를 구축하는 가장 유연한 방법입니다. 장치 화면 크기뿐만 아니라 실제 뷰어 크기도 타깃팅할 수 있습니다. 이는 반응형 디자인 웹 페이지 레이아웃에 유용할 수 있습니다.

**CSS 미디어 쿼리**

장치 감지는 순수 CSS 미디어 쿼리를 사용하여 수행할 수도 있습니다. 지정된 미디어 쿼리 블록 내에 포함된 모든 내용은 해당 장치에서 실행될 때만 적용됩니다.

Mobile Viewer에 적용되는 경우 CSS에 정의된 4개의 CSS 미디어 쿼리를 다음 순서로 사용하십시오.

1. 모든 터치 장치에 대한 규칙만 포함합니다.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. 고해상도 화면이 있는 태블릿에 특정한 규칙만 포함합니다.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. 모든 휴대폰에 대한 규칙만 포함합니다.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 고해상도 화면이 있는 휴대폰에 대한 규칙만 포함합니다.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

미디어 쿼리 접근 방식을 사용하면 다음과 같이 디바이스 감지로 CSS를 구성해야 합니다.

* 먼저, 바탕 화면별 섹션은 바탕 화면별 속성이거나 모든 화면에 공통되는 모든 속성을 정의합니다.
* 두 번째로, 4개의 미디어 쿼리는 위에 정의된 순서대로 실행되며 해당 디바이스 유형에 맞는 CSS 규칙을 제공합니다.

각 미디어 쿼리에서 전체 뷰어 CSS를 복제할 필요가 없습니다. 지정된 장치에 특정한 속성만 미디어 쿼리 내에 다시 정의됩니다.

## CSS 스프라이트 {#section-b0af39db1af74561aea9fddcc8cdc2c7}

대부분의 뷰어 사용자 인터페이스 요소는 비트맵 아트웍을 사용하여 스타일이 지정되며 둘 이상의 고유한 시각적 상태를 갖습니다. 좋은 예는 일반적으로 &quot;up&quot;, &quot;over&quot; 및 &quot;down&quot;의 세 가지 이상 다른 상태를 갖는 단추입니다. 각 상태에는 고유한 비트맵 아트워크가 할당되어야 합니다.

스타일링에 대한 클래식 접근 방식을 사용하면 CSS에는 사용자 인터페이스 요소의 각 상태에 대해 서버의 개별 이미지 파일에 대한 별도의 참조가 있습니다. 다음은 스크롤 단추 스타일을 지정하는 샘플 CSS입니다.

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-image:url(images/v2/ScrollLeftButton_up.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-image:url(images/v2/ScrollLeftButton_down.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-image:url(images/v2/ScrollLeftButton_disabled.png);  
}
```

이 접근 방식의 단점은 요소가 와 처음 상호 작용할 때 최종 사용자가 깜박이거나 지연된 사용자 인터페이스 응답을 경험한다는 것입니다. 이 작업은 새 요소 상태에 대한 이미지 아트워크가 아직 다운로드되지 않았기 때문에 발생합니다. 또한 이 방법은 서버에 대한 HTTP 호출 수가 증가하므로 성능에 약간 부정적인 영향을 줄 수 있습니다.

CSS 스프라이트는 모든 요소 상태에 대한 이미지 아트워크가 &quot;스프라이트&quot;라는 단일 PNG 파일로 결합되는 다른 방법입니다. 이러한 &quot;스프라이트&quot;는 지정된 요소에 대한 모든 시각적 상태를 차례로 배치합니다. 스프라이트를 사용하여 사용자 인터페이스 요소의 스타일을 지정할 때 CSS의 모든 다른 상태에 대해 동일한 스프라이트 이미지가 참조됩니다. 또한 `background-position` 속성은 각 상태에 대해 사용되는 &quot;스프라이트&quot; 이미지 부분을 지정하는 데 사용됩니다. 적절한 방법으로 &quot;스프라이트&quot; 이미지를 구조화할 수 있습니다. 뷰어는 일반적으로 세로로 스택되어 있습니다. 다음은 위에서 동일한 스크롤 단추를 스타일링하는 &quot;스프라이트&quot; 기반 예입니다.

```
.s7flyoutviewer .s7scrollleftbutton[state]  { 
    background-image: url(images/v2/ScrollLeftButton_light_sprite.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-position: -56px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-position: -0px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-position: -56px -448px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-position: -0px -448px;  
}
```

## 일반 스타일 노트 및 조언 {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS를 사용하여 뷰어 사용자 인터페이스를 맞춤화할 때 `!IMPORTANT` 규칙은 스타일 뷰어 요소에 지원되지 않습니다. 특히, `!IMPORTANT` 뷰어 또는 Viewer SDK에서 제공하는 기본 또는 런타임 스타일을 무시하는 데 규칙을 사용하면 안 됩니다. 그 이유는 적절한 구성 요소의 동작에 영향을 줄 수 있기 때문입니다. 대신 적절한 특수성과 함께 CSS 선택기를 사용하여 이 참조 안내서에 설명되어 있는 CSS 속성을 설정해야 합니다.
* CSS 내의 외부 에셋에 대한 모든 경로는 뷰어 HTML 페이지 위치가 아닌 CSS 위치에 대해 확인됩니다. 기본 CSS를 다른 위치에 복사할 때에는 이 규칙에 유의하십시오. 기본 에셋도 복사하거나 사용자 지정 CSS 내의 경로를 업데이트합니다.
* 비트맵 아트웍의 기본 형식은 PNG입니다.
* 비트맵 아트웍은 다음을 사용하여 사용자 인터페이스 요소에 할당됩니다. `background-image` 속성.
* 다음 `width` 및 `height` 사용자 인터페이스 요소의 속성은 논리적 크기를 정의합니다. 에 전달된 비트맵의 크기입니다. `background-image` 논리적 크기에는 영향을 주지 않습니다.
* [Retina]와 같은 고해상도 화면의 픽셀 밀도를 높게 사용하려면 비트맵 아트웍을 논리적 사용자 인터페이스 요소 크기의 두 배로 지정합니다. 그런 다음 을 적용합니다. `-webkit-background-size:contain` 속성을 사용하여 논리적 사용자 인터페이스 요소 크기까지 배경을 축소합니다.
* 사용자 인터페이스에서 단추를 제거하려면 을(를) 추가합니다 `display:none` CSS 클래스로 복사합니다.
* CSS가 지원하는 색상 값에 다양한 형식을 사용할 수 있습니다. 투명도가 필요한 경우 형식을 사용합니다 `rgba(R,G,B,A)`. 그렇지 않으면 형식을 사용할 수 있습니다 `#RRGGBB`.

## 일반 사용자 인터페이스 요소 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

다음은 플라이아웃 뷰어에 적용되는 사용자 인터페이스 요소 참조 설명서입니다.
