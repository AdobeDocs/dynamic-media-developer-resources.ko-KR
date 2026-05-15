---
title: insertBefore,insertAfter
description: 노드 앞 또는 뒤에 XML을 설정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 20d27fa7-e98a-4f85-9e48-5fa9ad3102b7
TQID: 'https://experienceleague.adobe.com/5WqGL0gctYUgKJ9yO-3y5siw4Ptbjq7HHx8kgCn-GYE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 53
ht-degree: 1%

---

# insertBefore,insertAfter{#insertbefore-insertafter}

노드 앞 또는 뒤에 XML을 설정합니다.

`insertBefore=<xml>, insertAfter=<xml>`

FXG 노드 요소에 `s7:elementID`이(가) 정의되어 있으면 이 명령을 사용하여 해당 노드의 앞 또는 뒤에 XML 조각을 추가할 수 있습니다.

## 예 {#section-1fc8d4135ef94b60b838391e1568e70e}

다음과 같은 그룹 태그가 있는 경우:

`<Group visible="true" s7:elementID="inner_shape">`

그런 다음:

`insertBefore.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

결과:

`<Rect height="75" rotation="0" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" width="75" x="74.354" y="182.762"><fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill></Rect><Group s7:elementID="inner_shape" visible="true">`

`insertAfter.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

결과:

`<Group s7:elementID="inner_shape" visible="true"> <Rect ai:knockout="0" d:userLabel="Background" height="392.581" visible="true" width="319.953" x="0.75" y="0.75"> <fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill> </Rect>`
