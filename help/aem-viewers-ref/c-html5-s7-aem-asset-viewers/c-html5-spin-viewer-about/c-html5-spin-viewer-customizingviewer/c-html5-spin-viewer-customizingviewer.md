---
description: 스핀 뷰어에 대한 모든 시각적 사용자 지정 및 대부분의 비헤이비어 사용자 지정은 사용자 정의 CSS를 만들어 수행합니다.
keywords: responsive
seo-description: 스핀 뷰어에 대한 모든 시각적 사용자 지정 및 대부분의 비헤이비어 사용자 지정은 사용자 정의 CSS를 만들어 수행합니다.
seo-title: 회전 뷰어 사용자 정의
solution: Experience Manager
title: 회전 뷰어 사용자 정의
topic: Dynamic media
uuid: d951501c-d6da-454c-be2f-0887ffcac77c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---


# 회전 뷰어 사용자 지정{#customizing-spin-viewer}

스핀 뷰어에 대한 모든 시각적 사용자 지정 및 대부분의 비헤이비어 사용자 지정은 사용자 정의 CSS를 만들어 수행합니다.

권장 작업 과정은 적절한 뷰어에 대한 기본 CSS 파일을 가져와서 다른 위치에 복사하고 사용자 지정하고 `style=` 명령에서 사용자 지정된 파일의 위치를 지정하는 것입니다.

기본 CSS 파일은 다음 위치에 있습니다.

`<s7_viewers_root>/html5/SpinViewer_light.css`

뷰어는 &quot;라이트&quot; 및 &quot;다크&quot; 색상 구성표를 위한 기본 CSS 파일과 함께 제공됩니다. &quot;light&quot; 버전은 기본적으로 사용되지만 다음 표준 CSS를 사용하여 &quot;dark&quot; 버전으로 전환할 수 있습니다.

`<s7_viewers_root>/html5/SpinViewer_dark.css`

사용자 지정 CSS 파일은 기본 선언과 동일한 클래스 선언을 포함해야 합니다. 클래스 선언을 생략하면 사용자 인터페이스 요소에 대한 기본 스타일을 제공하지 않으므로 뷰어가 제대로 작동하지 않습니다.

사용자 지정 CSS 규칙을 제공하는 다른 방법은 웹 페이지 또는 연결된 외부 CSS 규칙 중 하나에서 직접 포함된 스타일을 사용하는 것입니다.

사용자 정의 CSS를 만들 때는 뷰어가 해당 컨테이너 DOM 요소에 `.s7spinviewer` 클래스를 할당한다는 것을 염두에 두십시오. `style=` 명령으로 전달된 외부 CSS 파일을 사용하는 경우 CSS 규칙에 대해 하위 선택기에서 `.s7spinviewer` 클래스를 상위 클래스로 사용합니다. 웹 페이지에서 포함된 스타일을 수행하는 경우 다음과 같이 컨테이너 DOM 요소의 ID를 사용하여 이 선택기의 자격을 추가로 지정합니다.

`#<containerId>.s7spinviewer`

## 반응형 디자인 CSS {#section-0bb49aca42d242d9b01879d5ba59d33b} 빌드

사용자의 장치 또는 특정 웹 페이지 레이아웃에 따라 다양한 장치를 타깃팅하고 CSS에 크기를 포함하여 내용이 다르게 표시되도록 할 수 있습니다. 다양한 웹 페이지 레이아웃, 유저 인터페이스 요소 크기 및 아트웍의 해상도를 포함하며 이에 국한되지 않습니다.

뷰어는 반응형 디자인 CSS를 만드는 두 가지 방법을 지원합니다.CSS 마커 및 표준 CSS 미디어 쿼리 이러한 메서드를 독립적으로 또는 함께 사용할 수 있습니다.

**CSS 마커**

반응형 디자인 CSS를 만드는 데 도움이 되도록 뷰어는 런타임 뷰어 크기 및 현재 장치에 사용된 입력 유형을 기반으로 최상위 뷰어 컨테이너 요소에 동적으로 할당되는 특수 CSS 클래스가 동적으로 할당된 CSS 마커를 지원합니다.

CSS 마커의 첫 번째 그룹에는 `.s7size_large`, `.s7size_medium` 및 `.s7size_small` 클래스가 포함됩니다. 뷰어 컨테이너의 런타임 영역에 따라 적용됩니다. 즉, 뷰어 영역이 일반적인 데스크톱 모니터 `.s7size_large`의 크기보다 크거나 같은 경우;영역 크기가 일반적인 태블릿 장치 `.s7size_medium`에 근접한 경우 휴대폰 화면과 유사한 영역의 경우 `.s7size_small`이(가) 설정됩니다. 이러한 CSS 마커의 주요 목적은 다양한 화면과 뷰어 크기에 맞는 서로 다른 유저 인터페이스 레이아웃을 만드는 것입니다.

CSS 마커의 두 번째 그룹에는 `.s7mouseinput` 및 `.s7touchinput`이 포함됩니다. `.s7touchinput` 현재 장치에 터치 입력 기능이 있는 경우 설정됩니다.그렇지 않은  `.s7mouseinput` 경우 가 사용됩니다. 일반적으로 터치 입력에는 더 큰 요소가 필요하므로 이러한 마커는 서로 다른 입력 유형에 대해 서로 다른 화면 크기의 사용자 인터페이스 입력 요소를 만들기 위한 것입니다. 장치에 마우스 입력 및 터치 기능이 모두 있는 경우 `.s7touchinput`이 설정되고 뷰어가 터치에 적합한 사용자 인터페이스를 렌더링합니다.

다음 샘플 CSS는 마우스 입력이 있는 시스템의 경우 단추 확대(zoom in) 크기를 28 x 28 픽셀, 터치 디바이스에서 56 x 56 픽셀)로 설정합니다. 또한 뷰어 크기가 매우 작으면 단추가 완전히 숨겨집니다.

```
.s7spinviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7spinviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7spinviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

픽셀 밀도가 다른 장치를 타깃팅하려면 CSS 미디어 쿼리를 사용합니다. 다음 미디어 쿼리 블록에는 고밀도 화면에만 적용되는 CSS가 포함됩니다.

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS 마커를 사용하는 것은 반응형 디자인 CSS를 빌드하는 가장 유연한 방법입니다. 따라서 장치 화면 크기만 아니라 실제 뷰어 크기를 대상으로 할 수 있으므로 반응형 디자인 페이지 레이아웃에 유용할 수 있습니다.

CSS 마커 접근 방식의 예로 기본 뷰어 CSS 파일을 사용합니다.

**CSS 미디어 쿼리**

장치 감지는 순수 CSS 미디어 쿼리를 사용하여 수행할 수도 있습니다. 지정된 미디어 쿼리 블록 내에 포함된 모든 항목은 해당 장치에서 실행되는 경우에만 적용됩니다.

모바일 뷰어에 적용할 때 CSS에 정의된 4개의 CSS 미디어 쿼리를 다음 순서로 사용합니다.

1. 모든 터치 장치에 대한 규칙만 포함합니다.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 고해상도 화면을 사용하는 태블릿에 대한 규칙만 포함합니다.

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

1. 고해상도 화면을 사용하는 휴대 전화에 대한 규칙만 포함합니다.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

미디어 쿼리 접근 방식을 사용하면 다음과 같이 장치 감지 기능을 사용하여 CSS를 구성해야 합니다.

* 먼저, 데스크톱 관련 섹션은 데스크톱 관련 속성이거나 모든 화면에 공통인 모든 속성을 정의합니다.
* 두 번째, 4개의 미디어 쿼리는 위에 정의된 순서대로 진행되며 해당 장치 유형에 맞는 CSS 규칙을 제공합니다.

각 미디어 쿼리에서 전체 뷰어 CSS를 복제할 필요가 없습니다. 지정된 장치에 고유한 속성만 미디어 쿼리 내에서 재정의됩니다.

## CSS 스프라이트 {#section-b671c70acf284cb0aea678c2d2e4babc}

많은 뷰어 사용자 인터페이스 요소는 비트맵 아트웍을 사용하여 스타일링되며 두 개 이상의 별개의 시각적 상태를 가집니다. 좋은 예는 일반적으로 3개 이상의 다른 상태를 갖는 단추입니다.&quot;up&quot;, &quot;over&quot; 및 &quot;down&quot; 각 상태에는 고유한 비트맵 아트웍이 할당되어야 합니다.

스타일 지정에 대한 클래식 접근 방식에서는 CSS가 사용자 인터페이스 요소의 각 상태에 대해 서버의 개별 이미지 파일에 대한 별도의 참조를 갖게 됩니다. 다음은 확대 단추 스타일링을 위한 샘플 CSS입니다.

```
.s7spinviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

이 접근 방식의 단점은 요소가 처음으로 상호 작용할 때 최종 사용자가 깜박이거나 지연된 사용자 인터페이스 응답을 경험할 수 있다는 것입니다. 이 작업은 새 요소 상태에 대한 이미지 아트웍이 아직 다운로드되지 않았기 때문에 발생합니다. 또한 이 접근 방식은 서버에 대한 HTTP 호출 수가 증가하여 성능에 다소 부정적인 영향을 줄 수 있습니다.

CSS 스프라이트는 모든 요소 상태에 대한 이미지 아트웍을 &quot;스프라이트&quot;라는 단일 PNG 파일로 결합하는 다른 접근 방식입니다. 이러한 &quot;스프라이트&quot;에는 지정된 요소가 차례로 배치된 모든 시각적 상태가 있습니다. 스프라이트가 있는 사용자 인터페이스 요소의 스타일을 지정할 때 CSS의 서로 다른 모든 상태에 대해 동일한 스프라이트 이미지가 참조됩니다. 또한 각 상태에 대해 `background-position` 속성을 사용하여 &quot;스프라이트&quot; 이미지의 어느 부분을 사용할지 지정합니다. &quot;스프라이트&quot; 이미지를 원하는 방식으로 구조화할 수 있습니다. 일반적으로 뷰어에는 세로로 쌓여 있습니다. 아래는 위에서 동일한 확대/축소 단추에 대한 스타일링을 &quot;스프라이트&quot; 기반으로 하는 예입니다.

```
.s7spinviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7spinviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## 일반적인 스타일 지정 참고 및 조언 {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS를 사용하여 뷰어 사용자 인터페이스를 사용자 지정할 때 뷰어 요소의 스타일을 지정하는 데 `!IMPORTANT` 규칙 사용이 지원되지 않습니다. 특히, `!IMPORTANT` 규칙은 뷰어 또는 뷰어 SDK에서 제공하는 기본 또는 런타임 스타일링을 재정의하는 데 사용해서는 안됩니다. 이유는 적절한 구성 요소의 동작에 영향을 줄 수 있기 때문입니다. 대신 적절한 특성으로 CSS 선택기를 사용하여 이 참조 안내서에 설명된 CSS 속성을 설정해야 합니다.
* CSS 내의 외부 에셋에 대한 모든 경로는 뷰어 HTML 페이지 위치가 아니라 CSS 위치에 대해 확인됩니다. 기본 CSS를 다른 위치에 복사할 때는 이 규칙을 알고 있어야 합니다. 기본 에셋을 복사하거나 사용자 지정 CSS 내에서 경로를 업데이트합니다.
* 비트맵 아트웍의 기본 형식은 PNG입니다.
* 비트맵 아트웍은 `background-image` 속성을 사용하여 사용자 인터페이스 요소에 할당됩니다.
* 사용자 인터페이스 요소의 `width` 및 `height` 속성은 논리적 크기를 정의합니다. `background-image`에 전달된 비트맵의 크기는 논리적 크기에 영향을 주지 않습니다.
* Retina와 같은 고해상도 화면의 높은 픽셀 밀도를 사용하려면 논리 유저 인터페이스 요소 크기보다 두 배 큰 비트맵 아트웍을 지정합니다. 그런 다음 `-webkit-background-size:contain` 속성을 적용하여 배경을 논리 사용자 인터페이스 요소 크기로 축소합니다.
* 사용자 인터페이스에서 버튼을 제거하려면 해당 CSS 클래스에 `display:none`을(를) 추가합니다.
* CSS에서 지원하는 색상 값에 다양한 형식을 사용할 수 있습니다. 투명도가 필요한 경우 `rgba(R,G,B,A)` 형식을 사용합니다. 그렇지 않으면 `#RRGGBB` 형식을 사용할 수 있습니다.

## 공통 사용자 인터페이스 요소 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

다음은 혼합 미디어 뷰어에 적용되는 사용자 인터페이스 요소 참조 설명서입니다.
