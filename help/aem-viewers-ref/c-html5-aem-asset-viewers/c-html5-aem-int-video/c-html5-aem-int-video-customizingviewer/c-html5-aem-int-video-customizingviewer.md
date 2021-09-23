---
title: 대화형 비디오 뷰어 사용자 지정
description: 대화형 비디오 뷰어에 대한 모든 시각적 사용자 지정 및 대부분의 동작 사용자 지정은 사용자 지정 CSS를 만들어 수행합니다.
keywords: 응답형
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c428c3e6-81be-4708-b064-f9d794183209
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 0%

---

# 대화형 비디오 뷰어 사용자 지정{#customizing-interactive-video-viewer}

대화형 비디오 뷰어에 대한 모든 시각적 사용자 지정 및 대부분의 동작 사용자 지정은 사용자 지정 CSS를 만들어 수행합니다.

제안된 워크플로우는 적절한 뷰어에 대한 기본 CSS 파일을 가져와 다른 위치에 복사하고 사용자 지정하고 `style=` 명령에서 사용자 지정된 파일의 위치를 지정하는 것입니다.

기본 CSS 파일은 다음 위치에 있습니다.

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

뷰어에는 &quot;light&quot; 및 &quot;dark&quot; 색상 구성표에 대한 두 개의 기본 CSS 파일이 제공됩니다. &quot;dark&quot; 버전은 기본적으로 사용되지만, 다음 표준 CSS를 사용하여 &quot;light&quot; 버전으로 쉽게 전환할 수 있습니다.

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

사용자 지정 CSS 파일은 기본 선언과 동일한 클래스 선언을 포함해야 합니다. 클래스 선언을 생략하면 사용자 인터페이스 요소에 대해 기본 스타일을 제공하지 않으므로 뷰어가 제대로 작동하지 않습니다.

사용자 지정 CSS 규칙을 제공하는 또 다른 방법은 웹 페이지나 연결된 외부 CSS 규칙 중 하나에 직접 포함된 스타일을 사용하는 것입니다.

사용자 지정 CSS를 만들 때는 뷰어가 해당 컨테이너 DOM 요소에 `.s7interactivevideoviewer` 클래스를 할당한다는 점에 유의하십시오. `style=` 명령으로 전달된 외부 CSS 파일을 사용하는 경우 CSS 규칙에 대해 하위 선택기에서 `.s7interactivevideoviewer` 클래스를 상위 클래스로 사용합니다. 웹 페이지에서 포함된 스타일을 수행하는 경우 컨테이너 DOM 요소의 ID로 이 선택기를 다음과 같이 분류하십시오.

`#<containerId>.s7interactivevideoviewer`

## 반응형 디자인 CSS 빌드 {#section-0bb49aca42d242d9b01879d5ba59d33b}

다양한 장치를 타깃팅하고 CSS에 포함 크기를 지정하여 사용자의 장치 또는 특정 웹 페이지 레이아웃에 따라 컨텐츠가 다르게 표시될 수 있습니다. 이 방법은 다양한 레이아웃, 사용자 인터페이스 요소 크기 및 아트워크 해상도를 포함하지만 이에 제한되지 않습니다.

뷰어는 반응형 디자인 CSS를 만드는 두 가지 메커니즘을 지원합니다. CSS 마커 및 표준 CSS 미디어 쿼리. 이러한 메커니즘을 독립적으로 또는 함께 사용할 수 있습니다.

**CSS 마커**

반응형 디자인 CSS를 만드는 데 도움이 되도록 뷰어는 CSS 마커를 지원합니다. 이러한 마커는 특수 CSS 클래스입니다. 런타임 뷰어 크기와 현재 장치에서 사용되는 입력 유형에 따라 최상위 뷰어 컨테이너 요소에 동적으로 할당됩니다.

CSS 마커의 첫 번째 그룹에는 `.s7size_large`, `.s7size_medium` 및 `.s7size_small` 클래스가 포함됩니다. 뷰어 컨테이너의 런타임 영역을 기반으로 적용됩니다. 뷰어 영역이 일반 데스크탑 모니터의 크기보다 크거나 같으면 `.s7size_large` 이 사용됩니다. 영역이 일반적인 태블릿 장치에 가까운 경우 `.s7size_medium`이 할당됩니다. 휴대폰 화면과 유사한 영역의 경우 `.s7size_small`이(가) 설정되어 있습니다. 이러한 CSS 마커의 주요 목적은 다양한 화면 및 뷰어 크기에 맞는 서로 다른 사용자 인터페이스 레이아웃을 만드는 것입니다.

두 번째 CSS 마커 그룹은 `.s7mouseinput` 및 `.s7touchinput`을 포함합니다. 마커 `.s7touchinput`은 현재 장치에 터치 입력 기능이 있는 경우 설정됩니다. 그렇지 않으면 `.s7mouseinput` 이 사용됩니다. 일반적으로 터치 입력에는 더 큰 요소가 필요하므로 이러한 마커는 대부분 다른 입력 유형에 대해 화면 크기가 다른 사용자 인터페이스 입력 요소를 만들기 위한 것입니다.

CSS 마커의 세 번째 그룹은 `.s7device_landscape` 및 `.s7device_portrait`을 포함합니다. 터치 장치가 가로 방향인 경우 마커 `.s7device_landscape`이 설정됩니다. `.s7device_portrait` 터치 장치가 세로 방향으로 회전할 때 사용됩니다. 이러한 CSS 마커는 데스크탑 시스템에서만 사용할 수 있습니다.

다음 샘플 CSS는 마우스 입력이 있는 시스템에서는 재생/일시 정지 단추 크기를 28x28 픽셀로 설정하고 터치 장치에서 56x56 픽셀로 설정합니다. 또한 뷰어 크기를 크게 줄이면 단추를 완전히 숨깁니다.

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7interactivevideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7interactivevideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

다음 예제에서는 터치 장치가 세로 방향인 경우 비디오 컨트롤 막대가 뷰어 아래쪽의 138픽셀 위에 있습니다. 다른 모든 경우 뷰어의 하단으로 이동됩니다.

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
}
```

픽셀 밀도가 다른 장치를 타깃팅하려면 CSS 미디어 쿼리를 사용해야 합니다. 다음 미디어 쿼리 블록에는 고집적 화면별 CSS가 포함됩니다.

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS 마커를 사용하면 장치 화면 크기뿐만 아니라 실제 뷰어 크기를 타겟팅할 수 있으므로 응답형 디자인 레이아웃에 유용한 응답형 디자인 CSS를 빌드하는 가장 유연한 방법입니다.

CSS 마커 접근 방식의 예로 기본 뷰어 CSS 파일을 사용할 수 있습니다.

**CSS 미디어 쿼리**

순수 CSS 미디어 쿼리를 사용하여 장치 센싱을 수행할 수도 있습니다. 지정된 미디어 쿼리 블록 내에 둘러싸인 모든 것은 해당 장치에서 실행되는 경우에만 적용됩니다.

모바일 뷰어에 적용할 때 아래 나열된 순서로 CSS에 정의된 4개의 CSS 미디어 쿼리를 사용합니다.

1. 모든 터치 장치에 대한 특정 규칙만 포함합니다.

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

1. 모든 휴대폰에 대한 특정 규칙만 포함합니다.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 고해상도 화면을 사용하는 휴대폰에 대한 규칙만 포함합니다.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

미디어 쿼리 방법을 사용하면 다음과 같이 장치 센싱으로 CSS를 구성해야 합니다.

* 먼저, 데스크탑별 섹션에서는 모든 화면에 대해 데스크탑별 또는 공통인 모든 속성을 정의합니다.
* 그리고 두 번째, 네 개의 미디어 쿼리는 위에 정의된 순서로 이동하고 해당 장치 유형에 고유한 CSS 규칙을 제공합니다.

각 미디어 쿼리에서 전체 뷰어 CSS를 복제할 필요가 없습니다. 지정된 장치에 고유한 속성만 미디어 쿼리 내에서 다시 정의됩니다.

## CSS Sprite {#section-9b6d8d601cb441d08214dada7bb4eddc}

많은 뷰어 사용자 인터페이스 요소는 비트맵 아트웍을 사용하여 스타일이 지정되며 두 개 이상의 고유한 시각적 상태를 갖습니다. 좋은 예는 일반적으로 세 개 이상의 서로 다른 상태를 갖는 단추입니다. &quot;up&quot;, &quot;over&quot; 및 &quot;down&quot; 각 상태에는 고유한 비트맵 아트웍이 할당됩니다.

스타일링에 대한 클래식 접근 방식으로, CSS는 사용자 인터페이스 요소의 각 상태에 대해 서버의 개별 이미지 파일에 대한 별도의 참조를 갖게 됩니다. 다음은 전체 화면 단추의 스타일을 지정하는 샘플 CSS입니다.

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

이 접근 방식의 단점은 요소가 처음으로 상호 작용할 때 최종 사용자가 깜박이거나 지연된 사용자 인터페이스 응답을 경험하는 것입니다. 이 작업은 새 요소 상태에 대한 이미지 아트웍이 아직 다운로드되지 않았기 때문에 발생합니다. 또한 이 접근 방식은 서버에 대한 HTTP 호출 수가 증가하여 성능에 다소 부정적인 영향을 줄 수 있습니다.

CSS 스프라이트는 모든 요소 상태에 대한 이미지 아트워크가 &quot;스프라이트&quot;라는 단일 PNG 파일에 결합되는 다른 접근 방법입니다. 이러한 &quot;sprite&quot;에는 서로 다른 위치에 배치된 지정된 요소에 대한 모든 시각적 상태가 있습니다. 스프라이트를 사용하여 사용자 인터페이스 요소에 스타일을 지정할 때 CSS의 다른 모든 상태에 대해 동일한 스프라이트 이미지가 참조됩니다. 또한 각 상태에 대해 `background-position` 속성을 사용하여 &quot;sprite&quot; 이미지의 어느 부분을 사용할지 지정합니다. 적합한 방식으로 &quot;스프라이트&quot; 이미지를 구성할 수 있습니다. 시청자는 보통 세로로 적층되어 있습니다. 다음은 이전에 동일한 전체 화면 단추에 스타일을 지정하는 &quot;Sprite&quot; 기반 예입니다.

```
.s7interactivevideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## 일반 스타일 노트 및 조언 {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS를 사용하여 뷰어 사용자 인터페이스를 사용자 지정할 때 뷰어 요소의 스타일을 지정하는 데 `!IMPORTANT` 규칙의 사용이 지원되지 않습니다. 특히 뷰어 또는 Viewer SDK에서 제공하는 기본 또는 런타임 스타일을 재정의하는 데 `!IMPORTANT` 규칙을 사용하지 않아야 합니다. 이유는 올바른 구성 요소의 동작에 영향을 줄 수 있기 때문입니다. 대신, 이 참조 안내서에 설명된 CSS 속성을 설정하려면 적절한 특성과 함께 CSS 선택기를 사용해야 합니다.

* CSS 내의 외부 자산에 대한 모든 경로는 뷰어 HTML 페이지 위치가 아니라 CSS 위치에 대해 확인됩니다. 기본 CSS를 다른 위치에 복사할 때에는 이 규칙을 알고 있어야 합니다. 기본 자산을 복사하거나 사용자 지정 CSS 내에서 경로를 업데이트합니다.
* 비트맵 아트웍의 기본 형식은 PNG입니다.
* 비트맵 아트웍은 `background-image` 속성을 사용하여 사용자 인터페이스 요소에 할당됩니다.
* 사용자 인터페이스 요소의 `width` 및 `height` 속성은 논리적 크기를 정의합니다. `background-image`에 전달된 비트맵의 크기는 논리적 크기에 영향을 주지 않습니다.

* Retina와 같은 고해상도 화면의 높은 픽셀 밀도를 사용하려면 논리 사용자 인터페이스 요소 크기보다 두 배 큰 비트맵 아트웍을 지정합니다. 그런 다음 `-webkit-background-size:contain` 속성을 적용하여 배경을 논리 사용자 인터페이스 요소 크기로 축소합니다.
* 사용자 인터페이스에서 단추를 제거하려면 해당 CSS 클래스에 `display:none`을 추가하십시오.
* CSS에서 지원하는 색상 값에 다양한 형식을 사용할 수 있습니다. 투명도가 필요한 경우 `rgba(R,G,B,A)` 형식을 사용하십시오. 그렇지 않으면 `#RRGGBB` 형식을 사용할 수 있습니다.

## 공통 사용자 인터페이스 요소 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

다음은 대화형 비디오 뷰어에 적용되는 사용자 인터페이스 요소 참조 설명서입니다.
