---
description: 플랫폼 서버 설정을 포함합니다.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# server.xml{#server-xml}

플랫폼 서버 설정을 포함합니다.

이 XML 파일을 수정할 때 유효한 XML 구문을 유지하기 위해 주의해야 합니다. 그렇지 않으면 플랫폼 서버를 시작할 수 없습니다.

변경 사항을 적용하려면 이 파일을 편집한 후 플랫폼 서버를 다시 시작해야 합니다.

다음 다이어그램은 이 파일에서 변경할 수 있는 설정을 보여줍니다. 이러한 설정에 대한 설명은 이 문서의 해당 섹션을 참조하십시오. 이 다이어그램은 [!DNL server.xml]의 완전한 표현이 아닙니다.

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

