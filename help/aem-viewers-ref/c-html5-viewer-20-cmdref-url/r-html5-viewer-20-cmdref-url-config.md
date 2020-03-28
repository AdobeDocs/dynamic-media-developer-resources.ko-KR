---
description: 모든 뷰어에 공통으로 사용되는 매개 변수입니다.
seo-description: 모든 뷰어에 공통으로 사용되는 매개 변수입니다.
seo-title: config
solution: Experience Manager
title: config
topic: Dynamic media
uuid: 9e9bb580-a33a-4405-b05c-56962d702145
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# config{#config}

모든 뷰어에 공통으로 사용되는 매개 변수입니다.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId </span></span> </p> </td> 
   <td colname="col2"> <p>뷰어 구성의 카탈로그/ID입니다. </p> <p> 카탈로그::UserData의 뷰어 구성 속성을 포함하는 이미지 카탈로그 항목을 <span class="codeph"> 지정합니다 </span>. 이 명령이 있으면 뷰어는 구성 ID에 대한 <span class="codeph"> req=userdata </span> 명령을 <span class="codeph"> 서버에 보내고 </span> 응답에서 속성을 추출합니다. 속성은 뷰어를 초기화하는 데 사용됩니다. URL 문자열이 동일한 속성을 지정하면 <span class="codeph"> catalog::UserData의 값을 덮어씁니다 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

예상, `catalog::UserData``asset`, `serverUrl``contentUrl`, `searchServerUrl``config` 자체 등으로 지정할 수 있는 모든 뷰어 명령

## 속성 {#section-10ee45d637134e0fbcd943c62578cb78}

선택 사항입니다.

## 기본값 {#section-d411e450028c460392cb8508f8ccc5d9}

없음.

## 예제 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

2020이라는 이미지 카탈로그에는 항목이 `preset-oct`포함되어 있습니다. 이 카탈로그 항목의 `catalog::UserData` 필드에는 다음 데이터가 포함됩니다.

```
style=customStyle.css
```

다음 명령을 사용하여 뷰어를 로드합니다.

```
config=2020/preset-oct
```

이는 URL에 명시적으로 지정된 다음 명령에 해당합니다.

```
style=customStyle.css
```

## 예 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

2019라는 이미지 카탈로그에는 항목이 `spin-oct`포함되어 있습니다. 이 카탈로그 항목의 `catalog::UserData` 필드에는 다음 데이터가 포함됩니다.

```
zoomStep=3 
maxZoom=200
```

다음 명령을 사용하여 뷰어를 로드합니다.

```
config=2019/spin-oct
```

이는 URL에 명시적으로 지정된 다음 명령에 해당합니다.

```
zoomStep=3&maxZoom=200
```

## Example 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

이름이 지정된 뷰어 사전 설정에 `Shoppable_Banner` 다음 데이터가 포함됩니다.

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

다음 명령을 사용하여 뷰어를 로드합니다.

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

이는 URL에 명시적으로 지정된 다음 명령에 해당합니다.

`style=etc/dam/presets/css/html5_interactiveimage.css`

## Example 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

이름이 지정된 뷰어 사전 설정에 `Shoppable_Video_Dark` 다음 데이터가 포함됩니다.

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

다음 명령을 사용하여 뷰어를 로드합니다.

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

이는 URL에 명시적으로 지정된 다음 명령에 해당합니다.

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Example 5 {#section-19b988551d1d492a9079948e0b04b38f}

다음 데이터라는 뷰어 사전 `Carousel_Dotted_light` 설정:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

다음 명령을 사용하여 뷰어를 로드합니다.

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

이는 URL에 명시적으로 지정된 다음 명령에 해당합니다.

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

