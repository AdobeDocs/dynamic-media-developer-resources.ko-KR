---
title: AssetContextStateUpdate
description: 자산과 연결된 게시 컨텍스트에 대한 새 게시 상태 플래그 집합을 설정합니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

자산과 연결된 게시 컨텍스트에 대한 새 게시 상태 플래그 집합을 설정합니다.

**매개 변수**

| 이름 | 유형 | 설명 |
|---|---|---|
| assetHandle | `xsd:string` | 업데이트할 자산을 처리합니다. |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | 업데이트할 에셋의 게시 연락처 상태 배열입니다. |
