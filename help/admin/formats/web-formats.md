---
description: HTTP 데이터 파일을 만드는 데 사용할 수 있는 매크로를 나열합니다. HTTP는 JSON 형식으로 데이터를 전송합니다.
seo-description: Lists the macros you can use to create HTTP data files. HTTP sends data in a JSON format.
seo-title: HTTP Format Macros
title: HTTP 형식 매크로
uuid: 91021f60-75d0-4b1d-86ca-91c9dadafac1
exl-id: 80ed24ac-1b84-4c1b-966f-039b587ea899
source-git-commit: cfc3396843592d80b017471a0e88cf335a5f81e0
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 2%

---

# HTTP 형식 매크로 {#http-format-macros}

[!DNL HTTP]개의 데이터 파일을 만드는 데 사용할 수 있는 매크로를 나열합니다. [!DNL HTTP]이(가) 데이터를 [!DNL JSON] 형식으로 보냅니다.

일반적으로 사용되는 일부 매크로 조합의 목록 및 예제는 [HTTP 형식 매크로 예제](../formats/web-format-examples.md)를 참조하십시오.

<table id="table_72A72EA63C3643FB84B47A76CD2CC1CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 매크로 </th> 
   <th colname="col2" class="entry"> 메서드 유형 </th> 
   <th colname="col3" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>AAM_UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p> <span class="keyword"> Audience Manager </span> ID입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>데이터 파트너 고유 사용자 ID. 이 매크로는 <span class="keyword"> Audience Manager </span> 장치 ID와 ID가 이미 동기화된 경우 사용자에게 할당한 ID를 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>데이터 공급자 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ECID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>데이터 공급자 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>GENERATION_TIME</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>Unix UTC 타임스탬프. AAM 내부 타임스탬프는 <span class="wintitle"> S2S </span> 대상을 파트너에 게시하라는 알림을 받은 시간을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>IP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자의 IP 주소입니다. </p> </td> 
  </tr>
    <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Experience Cloud ID. (MCID는 Marketing Cloud을 의미하며, 이는 Experience Cloud의 기존 이름입니다.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_REMOVED_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 더 이상 속하지 않는 세그먼트의 수(정수)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 속한 세그먼트의 수입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>주문 또는 대상 ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID_ALIAS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>파트너 ID에 대한 별칭입니다. 외부 계정 ID라고도 합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>RANDOM</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>난수 생성. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REGION_ID_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>활동이 시작된 <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-regions.html?lang=ko"> Audience Manager DCS 영역 </a>입니다.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 더 이상 사용할 수 없는 세그먼트 ID 목록(있는 경우)을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 더 이상 사용할 수 없는 세그먼트 목록입니다. 다음을 포함하는 특정 세그먼트 필드를 반환할 수도 있습니다. </p> <p> 
     <ul id="ul_29B83093A7624A908F0C06F2A248981A"> 
      <li id="li_57A60A54F5D44E38ACB4E2648095F246"> <code>traitAlias</code> </li> 
      <li id="li_4079F646493F40DBA0CE75D662A69454"> <code>legacySegmentId (formerly segmentId)</code> </li> 
      <li id="li_D3509A2D379E4C1FB3BC1B5E7D45A916"> <code>newSegmentId</code> </li> 
      <li id="li_EA901C20EEEB4CFAA39A5E0E822D2394"> <code>status</code> </li> 
      <li id="li_6310E21F88CC4691980DD3C9D551409F"> <code>dateTime</code> </li> 
     </ul> </p> <p>다음 예제와 같이 배열에서 이러한 필드를 지정합니다. </p> <p> <code>[&lt;REMOVED_SEGMENTS:{seg|&lt;OPEN_BRACKET&gt;"Mapping":&lt;seg.traitAlias&gt;,"Status:"&lt;seg.status&gt;, "Time":&lt;seg.dateTime&gt;,"LegacySegmentId":&lt;seg.LegacySegmentId&gt;, "NewSegmentId":&lt;seg.NewSegmentId&gt;&lt;CLOSE_BRACKET&gt;}; "separator=","&gt;]</code> </p> <p><a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP 형식 매크로 예제 </a>도 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_TIME_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> 사용자가 더 이상 사용할 수 없는 세그먼트에 대한 마지막 실현 목록입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_TRAITALIAS_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 더 이상 사용할 수 없는 세그먼트의 별칭 이름 목록입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>세그먼트 ID 목록을 반환합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>사용자가 자격을 갖는 세그먼트 목록입니다. 다음을 포함하는 특정 세그먼트 필드를 반환할 수도 있습니다. </p> <p> 
     <ul id="ul_9209683A8E0A4B8081E5EFA4602F743F"> 
      <li id="li_D796526C1C9E45BEA891D619539888C4"> <code>traitAlias</code> </li> 
      <li id="li_BF12E010E1AD432C84605B9817F209DD"> <code>legacySegmentId (formerly segmentId)</code> </li> 
      <li id="li_4A81E3B715254549B9EADB983A2FC32B"> <code>newSegmentId</code> </li> 
      <li id="li_1F01A60829DF4C87879D94299E1D589C"> <code>status</code> </li> 
      <li id="li_E52F10CD5A04487D81A4B1750B0DC4E3"> <code>dateTime</code> </li> 
     </ul> </p> <p>다음 예제와 같이 배열에서 이러한 필드를 지정합니다. </p> <p> <code>[&lt;SEGMENTS:{seg|&lt;OPEN_BRACKET&gt;"Mapping":&lt;seg.traitAlias&gt;,"Status:"&lt;seg.status&gt;, "Time":&lt;seg.dateTime&gt;,"LegacySegmentId":&lt;seg.LegacySegmentId&gt;, "NewSegmentId":&lt;seg.NewSegmentId&gt;&lt;CLOSE_BRACKET&gt;}; "separator=","&gt;]</code> </p> <p><a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP 형식 매크로 예제 </a>도 참조하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIME_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>마지막 실현 목록. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Unix, UTC 타임스탬프. 세그먼트의 마지막 실현을 나타냅니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAITALIAS_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>특정 세그먼트에 대한 별칭 이름 목록입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_AGENT</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>초기 요청의 사용자 에이전트. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>POST</code> </p> </td> 
   <td colname="col3"> <p><span class="keyword"> Audience Manager </span> 사용자 ID 목록입니다. 다음을 포함하는 특정 필드를 반환할 수도 있습니다. </p> 
    <ul id="ul_B6857D809FDC46749B7E745BD8C45F8E"> 
     <li id="li_F31CD82D16ED41FD82518141D90B5B35"> <code>user.aamUuid</code> </li> 
     <li id="li_623FA758C84D4A2D9B25C7FBE90F62B7"> <code>user.dpUuid</code> </li> 
     <li id="li_976B941908EB494EB476B5FB68B8972D"> <code>user.segments</code> </li> 
     <li id="li_D7E129833D1E4D59A554FFCE353924EE"> <code>user.removedSegments</code> </li> 
     <li id="li_8B3DD69D3FE3493492FC9F162812FCD5"> <code>user.userAgent</code> </li> 
     <li id="li_8C7EA05585A64141876DF169C31322FE"> <code>user.ip</code> </li> 
     <li id="li_678076A31A7743C480F718C9E7A07E99"> <code>user.dpuuids</code> </li> 
     <li id="li_B598A5AED28C4304972E51DBD4E480D8"> <code>user.timestamp</code> </li> 
     <li id="li_8424D540282F449CA5AF6B3CC343DDCB"> <code>user.random</code> </li>
     <li><code>user.regionIds</code></li> 
    </ul> <p>다음 예제와 같이 이러한 필드를 지정합니다. </p> <p> 
     <codeblock>
       "AAM_UUID": "&lt;user.aamUuid&gt;" 
"DataPartner_UUID": "&lt;user.dpUuid&gt;" 
     </codeblock> </p> <p>전체 예제는 <a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP 형식 매크로 예제 </a>을(를) 참조하십시오. </p> </td> 
  </tr>
 </tbody>
</table>
