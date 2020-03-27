---
description: 플랫폼 서버 설정을 포함합니다.
seo-description: 플랫폼 서버 설정을 포함합니다.
seo-title: server.xml
solution: Experience Manager
title: server.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# server.xml{#server-xml}

플랫폼 서버 설정을 포함합니다.

이 XML 파일을 수정할 때는 유효한 XML 구문을 유지하기 위해 주의해야 합니다. 그렇지 않으면 플랫폼 서버를 시작할 수 없습니다.

변경 사항을 적용하려면 이 파일을 편집한 후 플랫폼 서버를 다시 시작해야 합니다.

다음 다이어그램은 이 파일에서 변경할 수 있는 설정을 보여줍니다. 이러한 설정에 대한 설명은 이 문서의 해당 섹션을 참조하십시오. 이 다이어그램은 전체 표현이 아닙니다 [!DNL server.xml].

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

