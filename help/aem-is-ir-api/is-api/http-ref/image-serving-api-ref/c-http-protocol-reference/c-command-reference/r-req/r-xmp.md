---
description: XMP 메타데이터. 요청 경로에 지정된 이미지와 연결된 XMP 메타데이터를 반환합니다.
seo-description: XMP 메타데이터. 요청 경로에 지정된 이미지와 연결된 XMP 메타데이터를 반환합니다.
seo-title: xmp
solution: Experience Manager
title: xmp
topic: Scene7 Image Serving - Image Rendering API
uuid: e1583ffe-531a-4334-b974-72df6fcb14ba
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 6%

---


# xmp{#xmp}

XMP 메타데이터. 요청 경로에 지정된 이미지와 연결된 XMP 메타데이터를 반환합니다.

`req=xmp`

다른 명령은 무시됩니다. UTF-8 인코딩이 적용됩니다. 응답은 MIME 유형이 `text/xml`인 XML로 지정됩니다.

HTTP 응답은 `catalog::Expiration`을(를) 기준으로 TTL을 사용하여 액세스할 수 있습니다.

## 속성 {#section-0d26b6a56c844153ae5cea4880370d00}

요청 속성을 참조하십시오. 현재 레이어 설정에 관계없이 적용됩니다.

## 기본값 {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

URL에 이미지 경로 또는 수정자가 포함되지 않은 경우:

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

그렇지 않은 경우 `req=img`

## 예제 {#section-34213692deab4a0f9037d5844132ee14}

이미지 파일 속성을 쿼리합니다.

` http:// *`서버`*/myPath/myImage.tif?req=imageprops`

이미지 카탈로그 속성 쿼리:

` http:// *`서버`*/myRootId?req=catalogprops`

HTML 파일에 포함된 클라이언트측 JavaScript에서 이미지 카탈로그 항목의 속성에 액세스합니다.

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

원래 크기의 25%로 크기가 조절된 특정 카탈로그 항목의 마스크 이미지를 검색합니다.

` http:// *`서버`*/myRootId/myImageId?req=mask&scale=0.25`

1-8번째 크기로 이미지 요청:

` http:// *`서버`*/myRootId/myImageId?scl=8`

이것은 다음과 같습니다.

` http:// *`서버`*/myRootId/myImageId?req=img&scl=8`

이미지 카탈로그에 지정된 축소판 속성에 따라 이미지의 축소판을 요청합니다.

` http:// *`서버`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

서버 로그에 텍스트 메시지를 보냅니다.

` http:// *`서버`*/myRootId?req=message&message=This%20is%20the%20message`

## 참조 {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [카탈로그::Target](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md),  [카탈로그::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md),  [축소판 크기 조정](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)  [ ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)  [,PropertiesPropertiesImage Map](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
