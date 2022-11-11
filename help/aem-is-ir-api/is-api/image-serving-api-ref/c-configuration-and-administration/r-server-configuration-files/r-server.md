---
description: 플랫폼 서버 설정을 포함합니다.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# server.xml{#server-xml}

플랫폼 서버 설정을 포함합니다.

이 XML 파일을 수정할 때는 유효한 XML 구문을 유지하거나 그렇지 않으면 [!DNL Platform Server] 시작되지 않을 수 있습니다.

변경 사항을 적용하려면 [!DNL Platform Server] 이 파일을 편집한 후 다시 시작해야 합니다.

다음 다이어그램은 이 파일에서 변경할 수 있는 설정을 보여 줍니다. 이러한 설정에 대한 설명은 이 문서의 앞부분에서 해당 섹션을 참조하십시오. 이 다이어그램은 [!DNL server.xml].

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```
