---
description: 이 섹션에서는 HTTP 프로토콜 명령에 대해 설명합니다.
seo-description: 이 섹션에서는 HTTP 프로토콜 명령에 대해 설명합니다.
seo-title: 명령 참조
solution: Experience Manager
title: 명령 참조
topic: Scene7 Image Serving - Image Rendering API
uuid: 72c4ed61-3436-4df5-b586-77808fb1903a
translation-type: tm+mt
source-git-commit: c5bac2c6e3f3a05bf69924072c4305dbd7ba1f4f
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 10%

---


# 명령 참조{#command-reference}

이 섹션에서는 HTTP 프로토콜 명령에 대해 설명합니다.

**AEM의 Dynamic Media에만 해당**:사용자 인터페이스에서 사용할 수 있는 기본 이미지 설정 외에도 AEM() [!DNL Dynamic Media] 에서 이미지 수정 필드에 지정할 수 있는 다양한 고급 이미지 수정 [!DNL Adobe Experience Manager]을  **** 지원합니다. 이러한 매개 변수는 아래에 정의되어 있습니다. 그러나 다음 기능은 AEM의 Dynamic Media에서 지원되지 않습니다.

* 색상 교정 명령:`icc=` 및 `iccEmbed=`.
* 기본 템플릿 및 텍스트 렌더링 명령:`text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` 및 `textPs=`.
* 현지화 명령:`locale=` 및 `req=xlate`.
* `req=set` 은(는) 일반적인 사용에 사용할 수 없습니다.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 비코어 Dynamic Media 서비스:SVG, 이미지 렌더링 및 Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

AEM 6.5 설명서의 Dynamic Media [이미지 사전 설정 옵션](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/managing-image-presets.html#image-preset-options)을 참조하십시오.

* [정렬](r-align.md)
* [앵커](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [캐시](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [자르기](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [효과](r-effect.md)
* [effectMask](r-effectmask.md)
* [extend](r-extend.md)
* [맞춤](r-fit.md)
* [flip](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [숨기기](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [레이어](r-layer.md)
* [로케일](r-locale.md)
* [맵](r-map.md)
* [마스크](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_grow](r-op-grow.md)
* [op_growMask](r-op-growmask.md)
* [op_growMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_noise](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [기원](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [원근](r-perspective.md)
* [오퍼](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [수량화](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [rotate](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
* [크기](r-size-reference.md)
* [src](r-src.md)
* [템플릿](r-template.md)
* [텍스트](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
