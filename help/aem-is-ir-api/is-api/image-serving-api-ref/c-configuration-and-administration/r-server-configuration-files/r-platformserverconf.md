---
description: ' [!DNL Platform Server] 설정을 포함합니다.'
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 00d55453-e7e6-4242-be83-7efa12764e5d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# PlatformServer.conf{#platformserver-conf}

[!DNL Platform Server] 설정을 포함합니다.

이 파일은 JAVA 속성 파일입니다. 적절한 규칙을 따르도록 주의해야 합니다. 그렇지 않으면 [!DNL Platform Server]을(를) 시작하지 못할 수 있습니다. Windows 파일 경로의 백슬래시 &#39;\\&#39; 대신 이중 백슬래시 &#39;\\&#39; 또는 단일 슬래시 &#39;/&#39;를 사용하십시오. 백슬래시는 이러한 유형의 파일에서 이스케이프 문자로 사용됩니다.

이 파일에 대한 변경 사항은 파일이 저장된 후에 적용됩니다.

아래 나열된 설정만 [!DNL PlatformServer.conf]에서 변경할 수 있습니다. 특정 설정이 없으면 파일의 아무 곳에나 추가할 수 있습니다. 각 설정의 인스턴스는 하나만 있을 수 있습니다.

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>일반 [!DNL Platform Server] 설정 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000 </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824 </span> </p> <p> <span class="codeph"> isConnection.port=27345 </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequests=true </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000 </span> </p> <p> <span class="codeph"> staticContent.rootPaths=./static-content </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>캐시 클러스터 구성 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;empty&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50 </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000 </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>오류 리디렉션 구성 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000 </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>SVG 구성 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./images </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024 </span> </p> <p> <span class="codeph"> svgProvider.port=8080 </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./images </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>미디어 집합 응답 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10 </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20 </span> </p> </td> 
 </tr> 
</table>
