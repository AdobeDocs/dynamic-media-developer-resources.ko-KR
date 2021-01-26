---
description: 노드 앞이나 뒤에 XML을 설정합니다.
seo-description: 노드 앞이나 뒤에 XML을 설정합니다.
seo-title: insertBefore,insertAfter
solution: Experience Manager
title: insertBefore,insertAfter
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5ac0f675-333b-4f85-abe0-642cf96de425
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 3%

---


# insertBefore,insertAfter{#insertbefore-insertafter}

노드 앞이나 뒤에 XML을 설정합니다.

`insertBefore=<xml>, insertAfter=<xml>`

FXG 노드 요소에 `s7:elementID`이 정의된 경우 이 명령을 사용하여 해당 노드 앞이나 뒤에 XML 조각을 추가할 수 있습니다.

## 예 {#section-1fc8d4135ef94b60b838391e1568e70e}

다음과 같은 그룹 태그가 있는 경우:

`<Group visible="true" s7:elementID="inner_shape">`

then:

`insertBefore.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

결과:

`<Rect height="75" rotation="0" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" width="75" x="74.354" y="182.762"><fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill></Rect><Group s7:elementID="inner_shape" visible="true">`

`insertAfter.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

결과:

`<Group s7:elementID="inner_shape" visible="true"> <Rect ai:knockout="0" d:userLabel="Background" height="392.581" visible="true" width="319.953" x="0.75" y="0.75"> <fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill> </Rect>`
