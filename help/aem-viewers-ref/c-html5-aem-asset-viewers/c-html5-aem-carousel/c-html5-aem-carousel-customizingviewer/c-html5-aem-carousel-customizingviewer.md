---
title: 슬라이드 뷰어 사용자 지정
description: 사용자 지정 CSS를 만들어 회전 뷰어 의 모든 시각적 사용자 지정 및 대부분의 비헤이비어 사용자 지정을 수행합니다.
keywords: 반응형
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f392d830-5c75-45dd-bab8-29a38218790d
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 0%

---

# 슬라이드 뷰어 사용자 지정{#customizing-carousel-viewer}

사용자 지정 CSS를 만들어 회전 뷰어 의 모든 시각적 사용자 지정 및 대부분의 비헤이비어 사용자 지정을 수행합니다.

제안된 워크플로는 적절한 뷰어에 대한 기본 CSS 파일을 가져와서 다른 위치에 복사하고, 사용자 지정하고, `style=` 명령에서 사용자 지정된 파일의 위치를 지정하는 것입니다.

기본 CSS 파일은 다음 위치에서 찾을 수 있습니다.

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

뷰어에는 각각 &quot;밝은&quot; 및 &quot;어두운&quot; 색상 체계의 숫자 및 점선 세트 표시기에 대한 4개의 기본 CSS 파일이 제공됩니다. 기본적으로 &quot;점선&quot; 버전이 사용되지만 다른 표준 CSS를 사용하고 `SetIndicator.mode` 매개 변수를 설정하여 다른 버전으로 쉽게 전환할 수 있습니다. 다른 표준 CSS는 다음 위치에서 찾을 수 있습니다.

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

사용자 지정 CSS 파일은 기본 클래스 선언과 동일한 클래스 선언을 포함해야 합니다. 클래스 선언을 생략하면 뷰어가 사용자 인터페이스 요소에 기본 스타일을 제공하지 않으므로 제대로 작동하지 않습니다.

사용자 지정 CSS 규칙을 제공하는 또 다른 방법은 웹 페이지에서 직접 또는 연결된 외부 CSS 규칙 중 하나에 포함된 스타일을 사용하는 것입니다.

사용자 지정 CSS를 만들 때는 뷰어가 해당 컨테이너 DOM 요소에 `.s7carouselviewer` 클래스를 할당한다는 점을 유의하십시오. `style=` 명령을 사용하여 전달된 외부 CSS 파일을 사용하는 경우 CSS 규칙의 하위 항목 선택기에서 `.s7carouselviewer` 클래스를 상위 클래스로 사용합니다. 웹 페이지에 임베드된 스타일을 추가하는 경우 다음과 같이 컨테이너 DOM 요소의 ID로 이 선택기의 자격을 얻으십시오.

`#<containerId>.s7carouselviewer`

## 응답형 디자인 CSS 구축 {#section-0bb49aca42d242d9b01879d5ba59d33b}

사용자의 장치 또는 특정 웹 페이지 레이아웃에 따라 컨텐츠를 다르게 표시하도록 다양한 장치와 CSS의 포함 크기를 타깃팅할 수 있습니다. 이 기술은 상이한 레이아웃, 사용자 인터페이스 요소 크기 및 아트워크 해상도를 포함하지만 이에 제한되지 않는다.

뷰어는 반응형 디자인 CSS를 만드는 두 가지 메커니즘, 즉 CSS 마커 및 표준 CSS 미디어 쿼리를 지원합니다. 이 두 메커니즘을 독립적으로 사용하거나 함께 사용할 수 있습니다.

**CSS 마커**

반응형 디자인 CSS를 만드는 데 도움이 되도록 뷰어는 CSS 마커를 지원합니다. 이러한 마커는 최상위 뷰어 컨테이너 요소에 동적으로 할당되는 특수 CSS 클래스입니다. 런타임 뷰어 크기와 현재 장치에서 사용되는 입력 유형을 기반으로 합니다.

CSS 마커의 첫 번째 그룹에는 `.s7size_large`, `.s7size_medium` 및 `.s7size_small` 클래스가 있습니다. 뷰어 컨테이너의 런타임 영역을 기반으로 적용됩니다. 예를 들어 뷰어 영역이 일반 데스크톱 모니터의 크기보다 크거나 같은 경우 `.s7size_large`을(를) 사용합니다. 영역이 일반적인 태블릿 장치에 가까운 경우 `.s7size_medium`을(를) 지정하십시오. 휴대폰 화면과 유사한 영역의 경우 `.s7size_small`을(를) 사용합니다. 이러한 CSS 마커의 주요 목적은 다양한 화면과 뷰어 크기에 대해 다양한 사용자 인터페이스 레이아웃을 만드는 것입니다.

CSS 표식의 두 번째 그룹에는 `.s7mouseinput` 및 `.s7touchinput`이(가) 포함되어 있습니다. 현재 장치가 터치 입력인 경우 CSS 마커 `.s7touchinput`이(가) 설정됩니다. 그렇지 않으면 `.s7mouseinput`이(가) 사용됩니다. 일반적으로 터치 입력에는 더 큰 요소가 필요하므로 이러한 마커는 대부분 다양한 입력 유형에 대해 화면 크기가 다른 사용자 인터페이스 입력 요소를 만들기 위한 것입니다.

다음 샘플 CSS는 마우스 입력이 있는 시스템의 경우 확대 단추 크기를 28 x 28픽셀로 설정하고 터치 입력 장치의 경우 56 x 56픽셀로 설정합니다. 뷰어의 크기가 훨씬 작은 경우 20 x 20픽셀로 설정됩니다.

```
.s7carouselviewer.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7carouselviewer.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7carouselviewer.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

픽셀 밀도가 다른 장치를 타깃팅하려면 CSS 미디어 쿼리를 사용해야 합니다. 다음 미디어 쿼리 블록에는 고밀도 화면과 관련된 CSS가 포함됩니다.

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS 마커를 사용하면 장치 화면 크기뿐만 아니라 실제 뷰어 크기를 타깃팅할 수 있으므로 응답형 디자인 CSS를 구축하는 가장 유연한 방법입니다. 이는 응답형 디자인 레이아웃에 유용합니다.

CSS 마커 접근 방식의 예로 기본 뷰어 CSS 파일을 사용할 수 있습니다.

**CSS 미디어 쿼리**

또한 순수 CSS 미디어 쿼리를 사용하여 디바이스 감지를 수행할 수도 있습니다. 지정된 미디어 쿼리 블록 내에 포함된 모든 내용은 해당 장치에서 실행될 때만 적용됩니다.

모바일 뷰어에 적용되면 아래에 나열된 순서로 CSS에 정의된 4개의 CSS 미디어 쿼리를 사용합니다.

1. 모든 터치 장치에 대한 규칙만 포함합니다.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 고해상도 화면이 있는 태블릿에 대한 규칙만 포함합니다.

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

## CSS 스타일 {#section-9b6d8d601cb441d08214dada7bb4eddc}

대부분의 뷰어 사용자 인터페이스 요소는 비트맵 아트웍을 사용하여 스타일이 지정되며 둘 이상의 고유한 시각적 상태를 갖습니다. 일반적으로 세 가지 이상의 다른 상태(`up`, `over` 및 `down`)가 있는 단추가 좋은 예입니다. 각 상태에는 고유한 비트맵 아트워크가 할당되어야 합니다.

스타일링에 대한 클래식 접근 방식을 사용하면 CSS에는 사용자 인터페이스 요소의 각 상태에 대해 서버의 개별 이미지 파일에 대한 별도의 참조가 있습니다. 다음은 확대 단추 스타일을 지정하는 샘플 CSS입니다.

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

이 접근 방식의 단점은 요소가 와 처음 상호 작용할 때 최종 사용자가 깜박이거나 지연된 사용자 인터페이스 응답을 경험한다는 것입니다. 이 작업은 새 요소 상태에 대한 이미지 아트워크가 아직 다운로드되지 않았기 때문에 발생합니다. 또한 이 방법은 서버에 대한 HTTP 호출 수가 증가하므로 성능에 약간 부정적인 영향을 줄 수 있습니다.

CSS 스프라이트는 모든 요소 상태에 대한 이미지 아트워크가 &quot;스프라이트&quot;라는 단일 PNG 파일로 결합되는 다른 방법입니다. 이러한 &quot;스프라이트&quot;는 지정된 요소에 대한 모든 시각적 상태를 차례로 배치합니다. 스프라이트를 사용하여 사용자 인터페이스 요소의 스타일을 지정할 때 CSS의 모든 다른 상태에 대해 동일한 스프라이트 이미지가 참조됩니다. 또한 `background-position` 속성은 각 상태에 대해 &quot;스프라이트&quot; 이미지의 어떤 부분을 사용할지 지정하는 데 사용됩니다. 적절한 방법으로 &quot;스프라이트&quot; 이미지를 구조화할 수 있습니다. 뷰어는 일반적으로 세로로 스택되어 있습니다.

다음은 동일한 핫스팟 아이콘을 스타일링하는 &quot;sprite&quot; 기반의 예입니다.

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## 일반 스타일 노트 및 조언 {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS를 사용하여 뷰어 사용자 인터페이스를 사용자 지정할 때 뷰어 요소의 스타일을 지정하는 데 `!IMPORTANT` 규칙을 사용할 수 없습니다. 특히 뷰어 또는 뷰어 SDK에서 제공하는 기본 스타일 또는 런타임 스타일을 재정의하는 데 `!IMPORTANT` 규칙을 사용하면 안 됩니다. 그 이유는 적절한 구성 요소의 동작에 영향을 줄 수 있기 때문입니다. 대신, 이 뷰어 참조 가이드에 설명된 CSS 속성을 설정하려면 적절한 특수성과 함께 CSS 선택기를 사용해야 합니다.
* CSS 내의 외부 에셋에 대한 모든 경로는 뷰어 HTML 페이지 위치가 아닌 CSS 위치에 대해 확인됩니다. 기본 CSS를 다른 위치에 복사할 때에는 이 규칙에 유의하십시오. 기본 에셋도 복사하거나 사용자 지정 CSS 내의 모든 경로를 업데이트합니다.
* 비트맵 아트웍의 기본 형식은 PNG입니다.
* 비트맵 아트웍은 `background-image` 속성을 사용하여 사용자 인터페이스 요소에 할당됩니다.
* 사용자 인터페이스 요소의 `width` 및 `height` 속성은 논리적 크기를 정의합니다. `background-image`에 전달된 비트맵의 크기는 논리적 크기에 영향을 주지 않습니다.
* [Retina]와 같은 고해상도 화면의 픽셀 밀도를 높게 사용하려면 비트맵 아트웍을 논리적 사용자 인터페이스 요소 크기의 두 배로 지정합니다. 그런 다음 `-webkit-background-size:contain` 속성을 적용하여 배경을 논리적 사용자 인터페이스 요소 크기까지 축소합니다.
* 사용자 인터페이스에서 단추를 제거하려면 해당 CSS 클래스에 `display:none`을(를) 추가하십시오.
* CSS가 지원하는 색상 값에 다양한 형식을 사용할 수 있습니다. 투명도가 필요한 경우 `rgba(R,G,B,A)` 형식을 사용하십시오. 그렇지 않으면 `#RRGGBB` 형식을 사용할 수 있습니다.

## 일반적인 사용자 인터페이스 요소 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

다음은 비디오 이미지 뷰어에 적용되는 사용자 인터페이스 요소 참조 설명서입니다.
