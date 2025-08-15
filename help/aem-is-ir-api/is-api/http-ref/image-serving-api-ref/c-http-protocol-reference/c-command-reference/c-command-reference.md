---
title: 명령 참조
description: 이 섹션에서는 HTTP 프로토콜 명령에 대해 설명합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 4%

---

# 명령 참조{#command-reference}

이 섹션에서는 HTTP 프로토콜 명령에 대해 설명합니다.

>[!TIP]
>
>Dynamic Media [_스냅숏_](https://snapshot.scene7.com/)을(를) 사용하여 Dynamic Media 이미지 수정자 및 스마트 이미징의 이점을 알아보십시오.
>
> 스냅샷은 최적화된 동적 이미지 제공을 위한 Dynamic Media의 기능을 보여 주도록 설계된 시각적 데모 도구입니다. 테스트 이미지 또는 Dynamic Media URL로 실험하여 다양한 Dynamic Media 이미지 수정자의 출력을 시각적으로 관찰하고 다음에 대한 스마트 이미징 최적화를 수행합니다.
>* 파일 크기(WebP 및 AVIF 게재 포함)
>* 네트워크 대역폭
>* DPR(장치 픽셀 비율)
>
>스냅숏을 사용하는 것이 얼마나 쉬운지 알아보려면 [스냅숏 교육 비디오](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=ko)를 재생하세요(3분 17초).


**Adobe Experience Manager의 Dynamic Media 전용** - 사용자 인터페이스에서 사용할 수 있는 기본 이미지 설정 외에 AEM([!DNL Dynamic Media])의 [!DNL Adobe Experience Manager]에서는 **이미지 수정자** 필드에서 지정할 수 있는 다양한 고급 이미지 수정 사항을 지원합니다. 이러한 매개 변수는 아래에 정의되어 있습니다. 그러나 AEM의 Dynamic Media에서는 다음 기능이 지원되지 않습니다.

* 색상 수정 명령: `icc=` 및 `iccEmbed=`.
* 기본 템플릿 및 텍스트 렌더링 명령: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` 및 `textPs=`.
* 지역화 명령: `locale=` 및 `req=xlate`.
* `req=set`은(는) 일반 사용에 사용할 수 없습니다.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 비핵심 Dynamic Media 서비스: SVG, 이미지 렌더링 및 Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

AEM 6.5 설명서에서 Dynamic Media [이미지 사전 설정 옵션](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html?lang=ko#dynamic)을 참조하십시오.

* [정렬](r-align.md)
* [앵커](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [블렌드 모드](r-blendmode.md)
* [캐시](r-is-http-cache.md)
* [클립 경로](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [자르기](r-crop.md)
* [자르기 경로](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [dpr](r-dpr.md)
* [효과](r-effect.md)
* [효과 마스크](r-effectmask.md)
* [확장](r-extend.md)
* [맞춤](r-fit.md)
* [뒤집기](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [숨기기](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [이미지 집합](r-imageset.md)
* [jpeg 크기](r-jpegsize.md)
* [레이어](r-layer.md)
* [로케일](r-locale.md)
* [맵](r-map.md)
* [마스크](r-mask.md)
* [마스크 사용](r-maskuse.md)
* [네트워크](r-network.md)
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
* [원근감](r-perspective.md)
* [pos](r-pos.md)
* [인쇄 영역](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [정량화](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [회전](r-rotate.md)
* [크기 조절](r-is-http-scale.md)
* [scl](r-scl.md)
* [크기](r-size-reference.md)
* [src](r-src.md)
* [템플릿](r-template.md)
* [텍스트](r-text.md)
* [텍스트 각도](r-textangle.md)
* [textAttr](r-textattr.md)
* [텍스트 흐름 경로](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [텍스트 경로](r-textpath.md)
* [textPs](r-textps.md)
* [유형](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
