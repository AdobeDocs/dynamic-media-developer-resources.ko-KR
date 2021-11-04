---
title: 스마트 자르기 비디오 뷰어 사용자 지정
description: 스마트 자르기 비디오 뷰어 사용자 지정
keywords: 응답형
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# 스마트 자르기 비디오 뷰어 사용자 지정{#customizing-smartcrop-video-viewer}

모든 시각적 사용자 지정 및 대부분의 동작 사용자 지정은 사용자 지정 CSS를 만들어 수행합니다.

제안된 워크플로우는 적절한 뷰어에 대한 기본 CSS 파일을 가져와 다른 위치에 복사하고 사용자 지정하고 `style=` 명령.

기본 CSS 파일은 다음 위치에 있습니다.

`<s7_viewers_root>/html5/SmartCropVideoViewer.css`

사용자 지정 CSS 파일은 기본 선언과 동일한 클래스 선언을 포함해야 합니다. 클래스 선언을 생략하면 사용자 인터페이스 요소에 대해 기본 스타일을 제공하지 않으므로 뷰어가 제대로 작동하지 않습니다.

사용자 지정 CSS 규칙을 제공하는 또 다른 방법은 웹 페이지나 연결된 외부 CSS 규칙 중 하나에 직접 포함된 스타일을 사용하는 것입니다.

사용자 지정 CSS를 만들 때 뷰어가 `.s7smartcropvideoviewer` 클래스 이름을 컨테이너 DOM 요소로 지정합니다. 와 함께 전달되는 외부 CSS 파일을 사용하는 경우 `style=` 명령, 사용 `.s7smartcropvideoviewer` 이 클래스는 CSS 규칙의 하위 선택기에서 상위 클래스로 사용됩니다. 웹 페이지에 스타일을 포함하는 경우 다음과 같이 컨테이너 DOM 요소의 ID로 이 선택기를 분류할 수도 있습니다.

`#<containerId>.s7smartcropvideoviewer`

## 반응형 디자인 CSS 빌드 {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

CSS에서 다른 장치를 타깃팅하여 사용자의 장치에 따라 콘텐츠가 다르게 표시될 수 있습니다. 이 타겟팅에는 다양한 사용자 인터페이스 요소 크기와 아트워크 해상도가 포함되지만 이에 제한되지 않습니다.

뷰어는 반응형 디자인 CSS를 만드는 두 가지 메커니즘을 지원합니다. CSS 마커 및 표준 CSS 미디어 쿼리. 이 두 메커니즘을 독립적으로 또는 함께 사용할 수 있습니다.

**CSS 마커**

반응형 디자인 CSS를 만드는 데 도움이 되도록 뷰어는 최상위 뷰어 컨테이너 요소에 동적으로 할당된 특수 CSS 클래스를 CSS 마커를 지원합니다. 이 할당은 런타임 뷰어 크기와 현재 장치에서 사용되는 입력 유형을 기반으로 합니다.

CSS 마커의 첫 번째 그룹은 다음과 같습니다 `.s7size_large`, `.s7size_medium`, 및 `.s7size_small` 클래스를 참조하십시오. They are applied based on the runtime area of the viewer container. That is, if the viewer area is equal to or bigger than the size of a common desktop monitor `.s7size_large` is used; if the area is close in size to a common tablet device `.s7size_medium` is assigned. 휴대폰 화면과 유사한 지역의 경우 `.s7size_small` 이(가) 설정되어 있습니다. 이러한 CSS 마커의 주요 목적은 다양한 화면 및 뷰어 크기에 맞는 서로 다른 사용자 인터페이스 레이아웃을 만드는 것입니다.

두 번째 CSS 마커 그룹은 다음을 포함합니다 `.s7mouseinput` 및 `.s7touchinput`. 마커 `.s7touchinput` 현재 장치에 터치 입력 기능이 있는 경우 설정됩니다. 그렇지 않으면 `.s7mouseinput` 이 사용됩니다. 이러한 마커는 일반적으로 터치 입력에는 더 큰 요소가 필요하므로 다른 입력 유형에 대해 화면 크기가 다른 사용자 인터페이스 입력 요소를 만들기 위한 것입니다. 장치의 마우스 입력과 터치 기능이 모두 있는 경우, `.s7touchinput` 가 설정되고 뷰어가 터치에 적합한 사용자 인터페이스를 렌더링합니다.

다음 샘플 CSS는 재생/일시 정지 단추 크기를 마우스 입력이 있는 시스템에서는 28 x 28픽셀, 터치 장치에서는 56 x 56픽셀로 설정합니다. 또한 뷰어 크기가 작으면 단추를 완전히 숨깁니다.

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7smartcropvideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7smartcropvideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

다른 픽셀 밀도를 사용하는 장치를 타깃팅하려면 CSS 미디어 쿼리를 사용합니다. 다음 미디어 쿼리 블록에는 고집적 화면에만 적용되는 CSS가 포함됩니다.

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS 마커를 사용하는 것은 반응형 디자인 CSS를 빌드하는 가장 유연한 방법입니다. 이러한 유연성을 통해 장치 화면 크기뿐만 아니라 실제 뷰어 크기를 타겟팅할 수 있으므로 반응형 디자인 페이지 레이아웃에 유용할 수 있습니다.

CSS 마커 접근 방식의 예로 기본 뷰어 CSS 파일을 사용하십시오.

**CSS 미디어 쿼리**

순수한 CSS 미디어 쿼리를 사용하여 장치 감지를 수행할 수도 있습니다. 지정된 미디어 쿼리 블록 내에 둘러싸인 모든 것은 해당 장치에서 실행되는 경우에만 적용됩니다.

모바일 뷰어에 적용할 때 아래 나열된 순서로 CSS에 정의된 네 개의 CSS 미디어 쿼리를 사용합니다.

1. Contains only rules specific for all touch devices.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

CSS 미디어 쿼리 접근 방식을 사용하면 다음과 같이 장치 감지로 CSS를 구성해야 합니다.

* 먼저, 데스크탑별 섹션에서는 모든 화면에 대해 데스크탑별 또는 공통인 모든 속성을 정의합니다.
* 두 번째로, 네 개의 미디어 쿼리는 위에서 정의된 순서대로 이동하고 해당 장치 유형에 대한 CSS 규칙을 제공해야 합니다.

There is no need to duplicate the entire viewer CSS in each media query. 지정된 장치에 고유한 속성만 미디어 쿼리 내에서 다시 정의됩니다.

## CSS Sprite {#section-9b6d8d601cb441d08214dada7bb4eddc}

많은 뷰어 사용자 인터페이스 요소는 비트맵 아트웍을 사용하여 스타일이 지정되며 두 개 이상의 고유한 시각적 상태를 갖습니다. A good example is a button that normally has at least three different states: &quot;up&quot;, &quot;over&quot;, and &quot;down&quot;. 각 상태에는 고유한 비트맵 아트웍이 할당됩니다.

스타일링에 대한 클래식 접근 방식으로, CSS는 사용자 인터페이스 요소의 각 상태에 대해 서버의 개별 이미지 파일에 대한 별도의 참조를 갖게 됩니다. 다음은 전체 화면 단추의 스타일을 지정하는 샘플 CSS입니다.

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

이 접근 방식의 단점은 요소가 처음으로 상호 작용할 때 최종 사용자가 깜박이거나 지연된 사용자 인터페이스 응답을 경험하는 것입니다. 이 작업은 새 요소 상태에 대한 이미지 아트웍이 아직 다운로드되지 않았기 때문에 발생합니다. 또한 이 접근 방식은 서버에 대한 HTTP 호출 수가 증가하여 성능에 다소 부정적인 영향을 줄 수 있습니다.

CSS 스프라이트는 모든 요소 상태에 대한 이미지 아트워크가 &quot;스프라이트&quot;라는 단일 PNG 파일에 결합되는 다른 접근 방법입니다. 이러한 &quot;sprite&quot;에는 서로 다른 위치에 배치된 지정된 요소에 대한 모든 시각적 상태가 있습니다. 스프라이트를 사용하여 사용자 인터페이스 요소에 스타일을 지정할 때 CSS의 다른 모든 상태에 대해 동일한 스프라이트 이미지가 참조됩니다. 또한, `background-position` 속성은 각 상태에 대해 &quot;sprite&quot; 이미지의 어느 부분이 사용되는지를 지정하는 데 사용됩니다. 적합한 방식으로 &quot;스프라이트&quot; 이미지를 구성할 수 있습니다. 시청자는 보통 세로로 적층되어 있습니다. 다음은 위에서 동일한 전체 화면 단추에 스타일을 지정하는 &quot;Sprite&quot; 기반 예입니다.

```
.s7smartcropvideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## 일반 스타일 노트 및 조언 {#section-097418bd618740bba36352629e4d88e1}

* CSS 내의 외부 자산에 대한 모든 경로는 뷰어 HTML 페이지의 위치가 아닌 CSS 위치에 대해 확인됩니다. 기본 CSS를 다른 위치에 복사할 때에는 이 규칙을 기억하십시오. 기본 자산을 복사하거나 사용자 지정 CSS 내에서 경로를 업데이트합니다.
* 비트맵 아트웍의 기본 형식은 PNG입니다.
* 비트맵 아트웍은 `background-image` 속성을 사용합니다.
* 다음 `width` 및 `height` 사용자 인터페이스 요소의 속성은 논리 크기를 정의합니다. The size of the bitmap passed to `background-image` does not affect logical size.

* Retina와 같은 고해상도 화면의 높은 픽셀 밀도를 사용하려면 논리 사용자 인터페이스 요소 크기보다 두 배 큰 비트맵 아트웍을 지정합니다. 그런 다음 `-webkit-background-size:contain` 배경을 논리 사용자 인터페이스 요소 크기로 축소하는 속성입니다.
* 사용자 인터페이스에서 단추를 제거하려면 을(를) 추가합니다. `display:none` CSS 클래스로 가리키도록 업데이트하는 것이 좋습니다.
* CSS에서 지원하는 색상 값에 다양한 형식을 사용할 수 있습니다. 투명도가 필요한 경우 형식을 사용합니다 `rgba(R,G,B,A)`. 그렇지 않으면 형식을 사용할 수 있습니다 `#RRGGBB`.

* CSS를 사용하여 뷰어 사용자 인터페이스를 사용자 지정할 때 `!IMPORTANT` 스타일 뷰어 요소에는 규칙이 지원되지 않습니다. 특히, `!IMPORTANT` 규칙은 뷰어 또는 Viewer SDK에서 제공하는 기본 또는 런타임 스타일을 재정의하는 데 사용해서는 안 됩니다. 이유는 올바른 구성 요소의 동작에 영향을 줄 수 있기 때문입니다. 대신, 이 참조 안내서에 설명된 CSS 속성을 설정하려면 적절한 특성과 함께 CSS 선택기를 사용해야 합니다.

## 공통 사용자 인터페이스 요소 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

다음은 스마트 자르기 비디오 뷰어에 적용되는 사용자 인터페이스 요소 참조 설명서입니다.
