---
description: Audience Manager 관리 가이드에 대한 날짜별 모든 업데이트(추가, 삭제 및 수정 사항)입니다.
seo-description: All updates (additions, deletions, and corrections) to the Audience Manager Admin Guide, by date.
seo-title: Documentation Updates
title: 설명서 업데이트
uuid: 1c02dff5-8e3f-42bf-a50c-03b75e121ac7
exl-id: 8221b4df-99c2-47d3-a2ea-186a701a2b20
source-git-commit: 1f4dbf8f7b36e64c3015b98ef90b6726d0e7495a
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 94%

---

# 설명서 업데이트 {#documentation-updates}

Audience Manager 관리 가이드에 대한 날짜별 모든 업데이트(추가, 삭제 및 수정 사항)입니다.

기능 릴리스, 개선 사항 및 버그 수정에 대한 자세한 내용은 [Experience Cloud 릴리스 정보](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=en)를 참조하십시오. [!DNL Audience Manager] 설명서 변경 내용에 대해서는 [설명서 업데이트](https://experienceleague.adobe.com/docs/audience-manager/user-guide/documentation-updates/docs-2019.html?lang=en)를 참조하세요.

## AAM 2019 설명서 업데이트 {#aam-2019-docs-updates}

| 주제 | 설명 |
|--- |--- |
| HTTP 형식 매크로 | 새 매크로, `REGION_ID_LIST` 및 세 개의 새 필드,`sda`,`sda` 및 `sda`을 `USER_LIST` 매크로에 추가했습니다. |
| HTTP 형식 매크로 | 2개의 새 매크로(`ECID` 및 `MCID`)를 추가했습니다. |

## AAM 2018 설명서 업데이트 {#aam-2018-docs-updates}

<!-- c_doc_updates.xml -->

<table id="table_AECF59E131F84E7791A5A421BFB203FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 주제 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> FTP 서버 만들기 또는 편집</a> </p> </td> 
   <td colname="col2"> <p>SFTP 서버에 대해 SSH 키 인증에 자세한 정보를 추가했습니다(5단계). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-destination-troubleshooting.md#set-up-destinations-export"> Experience Cloud 내보내기 대상을 설정하는 방법...</a> </p> </td> 
   <td colname="col2"> <p>이 페이지에서는 아웃바운드 데이터 파일에서 원하는 ID 유형의 데이터를 내보내는 대상을 설정하는 방법을 보여 줍니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/admin-authorize-s3-cross-bucket.md#task_20B12994C5484A9D8CC40DF6F456CBE7"> 방법: 배치 대상에 대한 교차 계정 Amazon S3 버킷 액세스 권한 인증</a> </p> </td> 
   <td colname="col2"> <p>고객은 Amazon S3 액세스 키 및 비밀 키를 공유하지 않는 것을 선호하는 경우, 아웃바운드 데이터 파일을 전달하는 데 Amazon S3 계정간 버킷 권한을 사용할 수 있습니다. 이 문서에서는 Audience Manager 관리 UI에서 이 대체 요소를 설정하는 방법을 보여 줍니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2017 설명서 업데이트 {#aam-2017-docs-updates}

<table id="table_81D2DA9293A9417085C630D00A7C96E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 주제 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP 형식 매크로</a> </td> 
   <td colname="col2"><code>segmentId</code> 매크로를 <code>legacySegmentId</code>로 대체하고 <code>newSegmentId</code> 매크로를 추가했습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-company-limits.md#task_3004C10CB9A9430A8D25E25BB830B5D6"> 회사 제한 관리</a> </td> 
   <td colname="col2"> 최대 특성 폴더 번호 및 특성 구조 깊이를 제한 문서에 추가했습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="formats/enable-outbound-seq.md#concept_526744C9433F40BF8269E18245B2F0BD"> 아웃바운드에 대해 Hadoop 시퀀스 파일 전송 활성화</a> </td> 
   <td colname="col2"> 고객이 아웃바운드 시퀀스 파일을 자신의 Hadoop 인스턴스에 보낼 수 있도록 하는 방법을 확인하십시오. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967"> 컨테이너 관리</a> </td> 
   <td colname="col2"> 컨테이너를 만드는 방법에 대한 간단한 지침을 추가했습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-company-destinations.md#create-edit-company-destinations"> 회사 대상 만들기 또는 편집</a> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_527E0E75C03846B0AB39EEE544904BE2"> 
      <li id="li_FC276B34158D44E3A5450C6C8BAF3184">전체 및 증분 동기화 사용의 균형을 조정하는 방법에 대한 지침을 추가했습니다. </li> 
      <li id="li_3975DA78DE9E441D8F8CB80F752DD7B7"><span class="keyword">Audience Manager</span> 대상으로서의 <span class="keyword">Adobe Media Optimizaer</span> 프로비저닝은 <span class="keyword">Adobe Media Optimizer</span> 내에서 수행됩니다. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 회사 대상 관리</a> </p> </td> 
   <td colname="col2"> <p>경미한 수정. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-amo-sync.md#concept_2B5537233DAA4860B3503B344F937D83"> Media Optimizer와 ID 동기화</a> </p> </td> 
   <td colname="col2"> <p>각 회사 컨테이너의 AMO 동기화 확인란을 설명하는 새 설명서입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-device-graph-options.md#concept_563615F1018340C683E0EE075F8F639D"> 회사를 위한 장치 그래프 옵션</a> </p> </td> 
   <td colname="col2"> <p>장치 그래프 옵션을 구성하는 방법을 설명하는 새 설명서입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-oauth2/aam-admin-api-requirements.md#concept_A7FAC9443CF34974A873E6B787616421"> API 요구 사항 및 권장 사항</a> </p> </td> 
   <td colname="col2"> <p>고객을 파악하고 고객에게 전달해야 하는 일부 요구 사항과 권장 사항을 설명하는 새 설명서입니다. 동일한 제목과 다른 읽기 대상의 변경 사항이 있는 공개 문서에 복제됩니다. 공개 문서에서 <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html?lang=en#api-requirements-recommendations" format="https" scope="external">API 요구 사항 및 권장 사항</a>을 참조하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2016 설명서 업데이트 {#aam-2016-docs-updates}

<table id="table_E9D9810EA8244B58A4F27D56CFE521FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 주제 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> FTP 서버 만들기 또는 편집</a> </td> 
   <td colname="col2">송신 FTP IP <b>52.44.29.204</b>가 추가되었습니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 회사 대상 관리</a> </p> </td> 
   <td colname="col2"> <p>경미한 수정. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-http-server.md#task_5BF59581868E4144B965D644D36BEACD"> HTTP 서버 만들기 또는 편집</a> </p> </td> 
   <td colname="col2"> <p>서버 구성 만들기 마법사에 <b>HTTP 서명</b>을 추가했습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-beta-environment.md#concept_4AA12E66F49A452C8BA4E91AA28060AA"> 베타 환경</a> </p> </td> 
   <td colname="col2"> <p>베타 환경에서 URL 및 호스트 이름을 업데이트했습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/outbound-active-user-filter.md#task_F5CF8BDDA5DB4D23837B59CADF7A623B"> 활성 사용자로만 아웃바운드 데이터 필터링</a> </p> </td> 
   <td colname="col2"> <p>활성 사용자만 포함하는 전체 동기화 파일을 생성하는 지침 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP 형식 매크로</a> </p> </td> 
   <td colname="col2" morerows="1"> <p>HTTP 매크로 및 일반적인 예제를 나열하는 새 설명서입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP 형식 매크로 예제</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2015 설명서 업데이트 {#aam-2015-docs-updates}

<table id="table_90F524BAAED44A45A1F6BF8BBA9F26F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 및 주제 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2015년 12월 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 형식</a> </p> </td> 
   <td colname="col2"> <p>매크로 섹션을 수정하고 예제를 추가했습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2014 설명서 업데이트 {#aam-2014-docs-updates}

<table id="table_FA9962E19248418BA73D5A794A378C9D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 날짜 및 주제 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2014년 11월 12일 </p> <p> <a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 형식</a> </p> </td> 
   <td colname="col2"> <p>&lt;MCID&gt; 매크로에 대한 정보가 추가되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014년 10월 23일 </p> <p><a href="formats/admin-create-format.md#task_1A51FC9189DB439FB218D91F3875FD67"> 형식 만들기 또는 편집</a> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">.info Receipt </span>옵션에 대한 정보가 추가되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014년 10월 23일 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 형식</a> </p> </td> 
   <td colname="col2"> <p>새 페이지. 이 페이지는 현재 진행 중이며 며칠 후에 업데이트됩니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014년 10월 22일 </p> <p><a href="admin-destination-troubleshooting.md#"> 대상 설정 문제 해결</a> </p> </td> 
   <td colname="col2"> <p>새 주제입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014년 10월 21일 </p> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 회사 대상 관리</a> </p> </td> 
   <td colname="col2"> <p>전체 주제가 재구성되었습니다. 추가 정보 및 추가 설정이 추가되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014년 9월 25일 </p> <p><a href="companies/admin-manage-company-profiles.md"> 회사 만들기</a> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">라이프사이클</span> 및 <span class="wintitle">계정 유형</span> 섹션에 추가 정보가 추가되었습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014년 9월 25일 </p> <p><a href="companies/admin-manage-company-profiles.md#edit-company-profile"> 회사 프로필 편집</a> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">라이프사이클</span> 및 <span class="wintitle">계정 유형</span> 섹션에 추가 정보가 추가되었습니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
