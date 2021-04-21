---
description: 모든 뷰어에 공통되는 매개 변수입니다.
solution: Experience Manager
title: config
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 3%

---

# config{#config}

모든 뷰어에 공통되는 매개 변수입니다.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId  </span> </span> </p> </td> 
   <td colname="col2"> <p>뷰어 구성에 대한 카탈로그/ID. </p> <p> <span class="codeph"> 카탈로그::UserData </span>에 뷰어 구성 속성이 포함된 이미지 카탈로그 항목을 지정합니다. 이 명령이 있는 경우 뷰어는 <span class="codeph"> configId </span>에 대한 <span class="codeph"> req=userdata </span> 명령을 서버로 전송하고 응답에서 속성을 추출합니다. 속성은 뷰어를 초기화하는 데 사용됩니다. URL 문자열이 동일한 속성을 지정하면 <span class="codeph"> 카탈로그::UserData </span>의 값을 재정의합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

`catalog::UserData`에서 지정할 수 있는 모든 뷰어 명령은 `asset`, `serverUrl`, `contentUrl`, `searchServerUrl` 및 `config` 자체만 예상합니다.

## 속성 {#section-10ee45d637134e0fbcd943c62578cb78}

선택 사항입니다.

## 기본값 {#section-d411e450028c460392cb8508f8ccc5d9}

없음.

## 예제 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

2020이라는 이미지 카탈로그에는 `preset-oct` 항목이 포함되어 있습니다. 이 카탈로그 항목의 `catalog::UserData` 필드에 다음 데이터가 포함됩니다.

```
style=customStyle.css
```

다음 명령을 사용하여 뷰어를 로드합니다.

```
config=2020/preset-oct
```

이것은 URL에 명시적으로 지정된 다음 명령과 같습니다.

```
style=customStyle.css
```

## 예 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

2019라는 이미지 카탈로그에는 `spin-oct` 항목이 포함되어 있습니다. 이 카탈로그 항목의 `catalog::UserData` 필드에 다음 데이터가 포함됩니다.

```
zoomStep=3 
maxZoom=200
```

다음 명령을 사용하여 뷰어를 로드합니다.

```
config=2019/spin-oct
```

이것은 URL에 명시적으로 지정된 다음 명령과 같습니다.

```
zoomStep=3&maxZoom=200
```

## 예 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

`Shoppable_Banner`이라는 뷰어 사전 설정에는 다음 데이터가 포함됩니다.

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

다음 명령을 사용하여 뷰어를 로드합니다.

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

이것은 URL에 명시적으로 지정된 다음 명령과 같습니다.

`style=etc/dam/presets/css/html5_interactiveimage.css`

## 예 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

`Shoppable_Video_Dark`이라는 뷰어 사전 설정에 다음 데이터가 포함되어 있습니다.

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

다음 명령을 사용하여 뷰어를 로드합니다.

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

이것은 URL에 명시적으로 지정된 다음 명령과 같습니다.

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## 예 5 {#section-19b988551d1d492a9079948e0b04b38f}

다음 데이터인 `Carousel_Dotted_light` 뷰어 사전 설정:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

다음 명령을 사용하여 뷰어를 로드합니다.

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

이것은 URL에 명시적으로 지정된 다음 명령과 같습니다.

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```
