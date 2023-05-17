---
title: 명령 참조
description: 이 섹션에서는 HTTP 프로토콜 명령을 설명합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 187de979d7d1f7ce92b7b4c8b7661a787ab6889f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 6%

---

# 명령 참조{#command-reference}

이 섹션에서는 HTTP 프로토콜 명령을 설명합니다.

>[!TIP]
>
>Dynamic Media을 사용하여 Dynamic Media 이미지 수정자 및 스마트 이미징의 이점을 확인하고 살펴봅니다 [_스냅샷_](https://snapshot.scene7.com/).
>
> 스냅샷은 최적화 및 동적 이미지 전달을 위해 Dynamic Media의 강력한 기능을 보여주기 위해 설계된 시각적 데모 도구입니다. 다양한 Dynamic Media 이미지 수정자의 출력을 시각적으로 관찰하고 다음에 대한 스마트 이미징 최적화를 사용하여 테스트 이미지 또는 Dynamic Media URL을 실험합니다.
>* 파일 크기(WebP 및 AVIF 전달 포함)
>* 네트워크 대역폭
>* DPR (장치 픽셀 비율)
>
>스냅샷 사용 용이성을 알아보려면 [스냅샷 교육 비디오](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=en) (3분 17초).


**Adobe Experience Manager의 Dynamic Media에만 해당** - 사용자 인터페이스에서 사용할 수 있는 기본 이미지 설정 외에도, [!DNL Dynamic Media] AEM( [!DNL Adobe Experience Manager])에서는 에서 지정할 수 있는 다양한 고급 이미지 수정 사항을 지원합니다 **이미지 수정자** 필드. 이러한 매개 변수는 아래에 정의되어 있습니다. 그러나 AEM의 Dynamic Media에서는 다음 기능이 지원되지 않습니다.

* 색상 수정 명령: `icc=` 및 `iccEmbed=`.
* 기본 템플릿 및 텍스트 렌더링 명령: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` 및 `textPs=`.
* 로컬라이제이션 명령: `locale=` 및 `req=xlate`.
* `req=set` 은 일반적인 용도로 사용할 수 없습니다.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 비핵심 Dynamic Media 서비스: SVG, 이미지 렌더링 및 Web-to-Print

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Dynamic Media도 참조하십시오 [이미지 사전 설정 옵션](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) 를 참조하십시오.

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
* [확장](r-extend.md)
* [fit](r-fit.md)
* [뒤집기](r-flip.md)
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
* [원본](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [원근](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [수량](r-is-http-quantize.md)
* [recent](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [회전](r-rotate.md)
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
* [유형](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
