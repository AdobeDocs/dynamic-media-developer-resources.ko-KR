---
title: SearchFilter
description: 검색 기준을 정의하여 검색을 보다 효율적으로 만드는 데 도움이 되는 필터입니다.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b3a26966-33c9-48ca-b0ed-d05fc0e2050f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---

# [!DNL SearchFilter]{#searchfilter}

검색 기준을 정의하여 검색을 보다 효율적으로 만드는 데 도움이 되는 필터입니다.

구문

## 매개 변수 {#section-4c611d9bbe0d418d882632605fc4d29d}

<table id="table_57CEE262A33A4E898C6AFB30C93FD874"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이름 </th> 
   <th colname="col2" class="entry"> 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 폴더</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 검색할 폴더를 지정합니다. 회사 전체 및 전체를 검색하려면 비워 둡니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">다음으로 설정: 
    <ul id="ul_BD8686943BD14D05A21C00192D4D70D3"> 
     <li id="li_B6A6DE5AAEFF4A80A8413B4785A88222"><span class="codeph"> True</span>: 명명된 폴더 및 모든 하위 폴더를 검색합니다. </li> 
     <li id="li_10A581F98B4847ED8EBE4AECC3AD70A8"><span class="codeph"> False</span>: 명명된 폴더만 검색합니다. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">검색에서 반환할 에셋 유형의 목록입니다. 예: <span class="codeph"> 이미지</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3"> 검색에서 제외할 자산 유형을 지정합니다. 예를 들어 이미지가 그렇습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> type:StringArray</span> </td> 
   <td colname="col3">검색에서 반환할 에셋 하위 유형 목록입니다. 예를 들어 <span class="codeph"> Asset</span>의 경우 <span class="codeph"> MediaType</span> 하위 유형을 검색할 수 있습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p><span class="codeph"> assetSubTypeArray</span>이(가) 전달될 때 하위 유형이 없는 자산을 반환할지 여부를 지정하는 선택적 부울 플래그입니다. </p> <p>true이면 지정된 하위 유형 중 하나가 있는 자산만 반환됩니다. </p> <p>false인 경우 하위 유형이 없는 자산도 반환됩니다. </p> <p>기본값은 false입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">다음으로 설정: 
    <ul id="ul_8C164A5D9F0F43968C86A67FA6884F35"> 
     <li id="li_D8009688FF2C439D98D6C1052C1A6CBE"><span class="codeph"> True</span>: 원본 자산만 반환합니다. </li> 
     <li id="li_4970226BF0FF42388CAE4415FB63AF16"><span class="codeph"> False</span>: 생성된 콘텐츠를 반환합니다. 예: 업로드된 PDF의 이미지. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 검색할 프로젝트를 처리합니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">다음을 지정합니다. 
    <ul id="ul_96FFEE28F7624C1FB0356776B4C7CD53"> 
     <li id="li_DCB07288E5F44E05A4D83D3F34B0E08E">게시된 자산만 반환하도록 <span class="codeph"> MarkedForPublish</span>. </li> 
     <li id="li_9A9A852248DB490DB958AE986DF02672">게시되지 않은 자산만 반환하도록 <span class="codeph"> NotMarkedForPublish</span>. </li> 
    </ul> <p>참고: <i>모두</i> 게시된 상태 유형을 검색하려면 비워 두십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">다음을 지정합니다. 
    <ul id="ul_D31B903FA8DA4CFFABAFABA3D8DA91EC"> 
     <li id="li_E4386C8260E64F0BAFE5BA57FF788E48">휴지통 상태와 관계없이 자산을 반환하려면 <span class="codeph"> Any</span>. </li> 
     <li id="li_0B8933FE18C643828075EC8CE8C0223C"><span class="codeph"> NotInTrash</span>을(를) 사용하여 '일반' 자산을 반환합니다. </li> 
     <li id="li_A1F46A0762FA4D4BA9F7247338238DC6">휴지통에서 자산을 반환하려면 <span class="codeph"> InTrash</span>. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
