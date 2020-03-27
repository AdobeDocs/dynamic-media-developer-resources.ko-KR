---
description: 비디오 뷰어에 대한 구성 속성 설명서를 참조하십시오.
seo-description: 비디오 뷰어에 대한 구성 속성 설명서를 참조하십시오.
seo-title: 명령 참조 - 구성 속성
solution: Experience Manager
title: 명령 참조 - 구성 속성
topic: Dynamic media
uuid: 837cf230-f7dd-4010-a299-c3267d11e200
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 명령 참조 - 구성 속성{#command-reference-configuration-attributes}

비디오 뷰어에 대한 구성 속성 설명서를 참조하십시오.

URL에서 모든 구성 명령을 설정할 수 있습니다. 또는 API 메서드 `setParam()`또는 `setParams()`둘 모두를 사용하여 구성 명령을 설정할 수 있습니다. 서버측 구성 레코드에 구성 속성을 지정할 수도 있습니다.

일부 구성 명령에 클래스 이름 또는 해당 Viewer SDK 구성 요소의 인스턴스 이름으로 접두사를 지정할 수 있습니다. 구성 요소의 인스턴스 이름은 동적이며 API 메서드에 전달된 뷰어 컨테이너 DOM 요소의 ID에 따라 `setContainerId()` 달라집니다. 설명서에는 이러한 명령에 대한 선택적 접두사가 포함되어 있습니다. 예를 들어 다음과 같이 `playback` 문서화됩니다.

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

즉, 이 명령은 다음 방법으로 사용됩니다.

* `playback` (짧은 구문)
* `VideoPlayer.playback` (구성 요소 클래스 이름으로 적격)
* `cont_videoPlayer.playback` (구성 요소 ID로 적격, 컨테이너 요소의 ID `cont` 라고 가정하는 경우)

모든 [뷰어에 공통인 명령 참조 - 구성 속성](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

모든 [뷰어에 공통인 명령 참조 - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
