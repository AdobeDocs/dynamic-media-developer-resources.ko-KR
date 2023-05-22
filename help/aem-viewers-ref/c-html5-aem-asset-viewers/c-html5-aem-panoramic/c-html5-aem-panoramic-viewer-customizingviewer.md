---
title: 파노라마 뷰어 사용자 지정
description: 파노라마 뷰어에 대한 모든 시각적 사용자 지정 및 대부분의 비헤이비어 사용자 지정은 사용자 지정 CSS를 만들어 수행합니다.
keywords: 반응형
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Video360 Viewer 사용자 지정{#customizing-video-viewer}

모든 시각적 사용자 지정 및 대부분의 비헤이비어 사용자 지정은 사용자 지정 CSS를 만들어 수행합니다.

제안된 워크플로우는 적절한 뷰어에 대한 기본 CSS 파일을 가져와서 다른 위치에 복사하고, 사용자 지정하고, 에서 사용자 지정된 파일의 위치를 지정하는 것입니다. `style=` 명령입니다.

기본 CSS 파일은 다음 위치에서 찾을 수 있습니다.

`<s7viewers_root>/html5/PanoramicViewer.css`

사용자 지정 CSS 파일은 기본 클래스 선언과 동일한 클래스 선언을 포함해야 합니다. 클래스 선언을 생략하면 뷰어가 사용자 인터페이스 요소에 기본 스타일을 제공하지 않으므로 제대로 작동하지 않습니다.

사용자 지정 CSS 규칙을 제공하는 또 다른 방법은 웹 페이지에서 직접 또는 연결된 외부 CSS 규칙 중 하나에 포함된 스타일을 사용하는 것입니다.

사용자 지정 CSS를 만들 때는 뷰어가 `.s7panoramicviewer` 클래스를 컨테이너 DOM 요소에 추가합니다. 로 전달된 외부 CSS 파일을 사용하는 경우 `style=` 명령, 사용 `.s7panoramicviewer` 클래스를 CSS 규칙에 대한 하위 항목 선택기의 상위 클래스로 사용합니다. 웹 페이지에서 임베드된 스타일을 수행하는 경우 다음과 같이 컨테이너 DOM 요소의 ID로 이 선택기의 자격을 추가로 부여합니다.

`#<containerId>.s7panoramicviewer.`


## 일반 스타일 노트 및 조언 {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS 내의 외부 에셋에 대한 모든 경로는 뷰어 HTML 페이지 위치가 아닌 CSS 위치에 대해 확인됩니다. 기본 CSS를 다른 위치에 복사할 때 이를 고려하십시오. 기본 에셋도 복사하거나 사용자 지정 CSS 내의 경로를 업데이트해야 할 수 있습니다.
* CSS에서 지원하는 색상 값에 다양한 형식을 사용할 수 있습니다. 투명성이 필요한 경우, `rgba(R,G,B,A)` 형식이 권장됩니다. 그렇지 않으면 투명성이 요구되지 않습니다 `#RRGGBB` 를 사용할 수 있습니다.

CSS를 사용하여 뷰어 UI를 맞춤화할 때 `!IMPORTANT` 규칙은 스타일 뷰어 요소에 지원되지 않습니다. 특히, `!IMPORTANT` 규칙은 적절한 구성 요소 동작에 영향을 줄 수 있으므로 뷰어 또는 Viewer SDK에서 제공하는 기본 또는 런타임 스타일을 무시하는 데 사용해서는 안 됩니다. 대신, 이 참조 안내서에 설명된 CSS 속성을 설정하려면 적절한 특수성을 가진 CSS 선택기를 사용해야 합니다.

## 파노라마 뷰어 CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**기본 뷰어 영역**
주요 보기 영역은 파노라마 이미지가 차지하는 영역입니다.  크기를 지정하지 않은 경우 일반적으로 사용 가능한 장치 화면에 맞게 설정됩니다.

보기 영역의 모양은 CSS 클래스 선택기를 사용하여 제어됩니다.
`.s7panoramicviewer`

적용 가능한 CSS 속성은 다음과 같습니다.

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 뷰어의 너비; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 뷰어의 높이; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

예: 1024 x 512픽셀 크기의 뷰어를 설정합니다.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**파노라마 보기**
기본 보기는 파노라마 이미지로 구성됩니다.

기본 보기의 모양은 CSS 클래스 선택기를 사용하여 제어됩니다.
`.s7panoramicviewer .s7panoramicview`

적용 가능한 CSS 속성은 다음과 같습니다.
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 기본 보기의 배경색입니다. </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

예: 기본 보기를 투명하게 하려면 다음을 수행합니다.

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
