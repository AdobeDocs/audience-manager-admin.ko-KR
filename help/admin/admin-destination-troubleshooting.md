---
description: Audience Manager에서 대상을 설정하고 일반적인 문제를 방지하는 데 도움이 되는 정보입니다.
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: 대상 설정 문제 해결
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '1316'
ht-degree: 4%

---

# 대상 설정 문제 해결 {#destination-setup-troubleshooting}

Audience Manager에서 대상을 설정하고 일반적인 문제를 방지하는 데 도움이 되는 정보입니다.

## 대상을 설정했지만 파일이 표시되지 않습니다. 해당 세그먼트는 어디 있습니까? {#destination-no-files}

<!-- c_dest_tshooting.xml -->

일반적인 대상 구성 문제는 다음과 같습니다.

### 잘못 구성된 대상

* **잘못된  [!UICONTROL UserID] 키:**   [!UICONTROL UserID] 키 [!UICONTROL MasterDPID] 는 이 대상의 것이고, 경계를 지정할 ID 값의 기초입니다. 드롭다운 목록을 통해 [!UICONTROL UserID] 키를 선택할 수 있더라도 이 값에 매핑된 ID/트레이트/세그먼트가 반드시 있다는 뜻은 아닙니다. 대상이 만들어진 후 실행되는 [!UICONTROL Outbound] 프로세스가 이 [!UICONTROL UserID] 키에 매핑된 사용자를 찾지 못하면 데이터가 제한되지 않습니다.
* **선택한 파일 데이터 소스에 없음:** 이외의 대상 유형을 선택할 때  [!UICONTROL S2S]라는 레이블이 지정된 화면 하단에 섹션이 나타납니다  [!UICONTROL Configure Data Sources]. 이 섹션이 처음 나타나면 값이 선택되지 않습니다. [!UICONTROL All First Party] 확인란을 클릭하지 않거나 [!UICONTROL Available Data Sources] 창에서 개별적으로 데이터 소스를 선택하는 경우 데이터가 제한되지 않습니다.

### 잘못 구성된 형식

아웃바운드 데이터에 대한 형식을 선택할 때는 기존 형식을 다시 사용하는 것이 좋습니다. 이미 검증된 포맷을 사용하면 아웃바운드 데이터가 성공적으로 생성됩니다. 기존 형식의 형식을 정확하게 확인하려면 메뉴 모음에서 [!UICONTROL Formats] 옵션을 클릭하고 이름이나 ID 번호로 형식을 검색합니다. 형식이 잘못된 형식이나 형식으로 사용된 매크로가 잘못된 형식의 출력을 제공하거나 정보가 완전히 출력되지 않도록 합니다.

형식 설정 및 매크로 사용에 대한 자세한 내용은 [파일 형식 매크로](formats/file-formats.md#) 및 [HTTP 형식 매크로](formats/web-formats.md)를 참조하십시오.

### 잘못 구성된 서버

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * 호스트 이름에 접두사를 입력하지 마십시오. 계정 [!DNL ftp://hello.com]이 있는 경우 이 필드에 [!DNL hello.com]을 입력하면 됩니다.
   * **[!UICONTROL Port/Type Combination]**
      * [!DNL FTP] 전송의 경우 기본 전송 유형은 [!DNL SFTP]입니다.
      * [!DNL SFTP] 유형을 선택할 때 포트는 거의 항상 22입니다.
      * [!DNL FTPs/TLS] 유형을 선택할 때 포트는 거의 항상 21개입니다.
      * [!DNL FTPs/TLS] 유형은 일반 [!DNL FTP] 전송과 다릅니다. 일반(비보안) [!DNL FTP] 전송을 지원하지 않습니다.
   * **[!UICONTROL Remote Path]**
      * 원격 하위 경로를 선택할 때는 슬래시 없이 입력해야 합니다.
      * 전송된 파일을 [!DNL (root)/inbound] 하위 폴더에 배치해야 하는 경우에는 [!DNL /inbound] 이외의 원격 경로에 [!DNL inbound]을 추가하면 됩니다.
      * 파일을 경로에 여러 디렉토리를 보낼 경우 각 디렉토리 사이에 슬래시를 입력합니다. [!DNL /inbound/subdirectory1/subdirectory2] 위치가 지정되면 이 필드에 [!DNL inbound/subdirectory1/subdirectory2] 을 입력해야 합니다.
      * 파일을 외부 서버에 의해 자동으로 라우팅되는 디렉토리에 배치해야 하는 경우 이 공간을 비워 둘 수 있습니다. 기간( )은 입력하지 마십시오. ), 슬래시( / ) 또는 그 밖의 모든 것을 사용할 수 있습니다.

* **[!DNL S3]**
   * [!DNL S3] 는 기본 전송 프로토콜(또는  [!DNL FTP]  [!DNL HTTP]보다 큼)입니다.
      * **[!UICONTROL Bucket]**
         * 버킷 이름에는 슬래시, 접두사, 접미사 등이 없어야 합니다. 주소 [!DNL s3://your-bucket]이 지정된 경우 이 필드에 [!DNL your-bucket]을 추가하면 됩니다.
      * **[!UICONTROL Directory]**
         * 데이터를 배치해야 하는 하위 디렉터리가 특별히 지정되어 있지 않으면 이 필드를 비워 둡니다. 주소 [!DNL s3://your-bucket/your-subdirectory]이 지정된 경우 [!UICONTROL Bucket] 필드에 [!DNL your-bucket]을 입력하고 [!UICONTROL Directory] 필드에 [!DNL your-subdirectory]을 추가해야 합니다. 이전 슬래시를 추가하지 마십시오.
         * 여러 디렉토리를 경로에 이동해야 하는 경우에만 슬래시를 구분 기호로 사용해야 합니다. 따라서 [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] 위치는 [!UICONTROL Bucket] 필드에 [!DNL your-bucket], [!DNL your-subdirectory1/your-subdirectory2] 필드가 입력되어 있어야 합니다.[!UICONTROL Directory]
      * **[!UICONTROL Access / Secret Keys]**
         * [!DNL TechOps] 이 버킷을 생성하고 컨설턴트에게 액세스/비밀 키를 제공하면 이러한 자격 증명은 일반적으로 클라이언트에 전달되기 위한 `READ-ONLY` 자격 증명입니다. 이 자격 증명은 읽기 전용이므로 쓰기 불가능하므로 [!UICONTROL Access / Secret Key] 필드에 입력할 수 없습니다. [!DNL TechOps] 이 버킷을 생성하고 자격 증명을 제공하는 경우 컨설턴트는 또한 이 버킷에 파일을 작성할 수 있도록 해주는 Adobe 키 쌍(클라이언트에게 제공되지 않도록 함)도 요청해야 합니다. 해당 키를 이러한 필드에 추가해야 합니다.

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * [!DNL HTTP] 항목의 접두사 정보를 입력하십시오. 계정 [!DNL https://superduper.com]이 있는 경우 이 필드에 [!DNL https://superduper.com]을 입력합니다.
      * **[!UICONTROL URL Prefix]**
         * [!DNL URL] 접두사를 추가할 때는 이전 슬래시를 그대로 둡니다. [!DNL https://hello.com/r/x/y/z]의 주소에는 [!UICONTROL Domain] 필드에 [!DNL https://hello.com]을 입력하고 [!UICONTROL URL Prefix] 필드에 여기에 입력한 [!DNL r/x/y/z]이 있어야 합니다.
         * [!UICONTROL URL Prefix]이 필요하지 않으면 이 값을 비워 둡니다.
      * **[!UICONTROL Authentication - SSH Key]**
         * 정확한 암호화/키 저장을 위해 머리글, 바닥글 및 줄 바꿈을 포함하여 이 상자에 전체 `SSH PRIVATE` 키 값을 입력합니다.

### 아웃바운드 생성 시간이 충분하지 않음

아웃바운드 프로세스는 매일 두 번 실행되며 여러 프로세스(아웃바운드, 게시, 외부 위치로 푸싱 등)가 파일을 최종 대상으로 푸시하기 전에 실행해야 합니다. 경험상 데이터가 외부 위치로 푸시될 것을 기대하려면 적어도 24시간 전에 대상을 완전히 구성해야 합니다.

### 파일 분할 크기가 너무 큼

파일을 대상으로 보낼 때 큰 아웃바운드 파일을 파일 청크로 분할할 수 있습니다. 개별 파일 청크가 10GB를 초과하지 않도록 하십시오. 또한, [아웃바운드 데이터 파일 이름: 구문 및 예](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=en).


## 아웃바운드 데이터 파일에서 Experience Cloud ID, 고객 ID 또는 Audience Manager ID를 내보내기 대상을 설정하는 방법 {#set-up-destinations-export}

이 페이지에서는 [!UICONTROL Outbound Data Files]에서 원하는 ID 유형을 키로 사용하는 데이터를 내보낼 대상을 설정하는 방법을 보여 줍니다.

<!-- set-up-destinations-mcid-aamid.xml -->

대상은 Adobe 고객이 다양한 디지털 채널에서 데이터를 활성화할 수 있도록 해줍니다. 예를 들어 대상 데이터를 다른 [!DNL Adobe Experience Cloud] 솔루션([!DNL Target], [!DNL Campaign] 등)으로 내보낼 수 있습니다. 또는 [!UICONTROL DSP]s, [!UICONTROL SSP]s 또는 Audience Manager과 통합된 모든 플랫폼으로 데이터를 전송할 수 있습니다. Adobe에서는 [통합 Wiki 페이지](https://wiki.corp.adobe.com/display/MCPI)에서 함께 사용하는 파트너 목록을 보관합니다.

>[!NOTE]
>
>관리자 UI에서 대상 만들기에 대한 자세한 내용은 [회사 대상 만들기 또는 편집](companies/admin-manage-company-destinations.md#create-edit-company-destinations) 문서를 참조하십시오.

고객은 대상에 따라 다른 ID 유형을 내보내려고 합니다. 아래 구성 차트는 다른 ID 유형과 관련된 프로필 정보를 내보내기 위해 선택해야 하는 옵션을 보여줍니다. Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=en)의 [ID 색인도 참조하는 것이 좋습니다. 고려해야 할 세 가지 중요한 설정인 [!UICONTROL User ID Key], [!UICONTROL Data Source Type] 및 [!UICONTROL Format]가 있습니다. 모두 아래에 자세히 설명되어 있습니다.

* [!UICONTROL User ID Key]. [!UICONTROL Admin UI]에서 **[!UICONTROL Companies]**(으)로 이동합니다. 고객의 회사를 검색하고 클릭합니다. **[!UICONTROL Destinations]** 탭을 찾아 **[!UICONTROL Add Destination]** 키를 누릅니다. **[!UICONTROL Add Destination]** 워크플로우에서 [!UICONTROL User ID Key] 을(를) 선택합니다. [!UICONTROL User ID Key]은(는) 대상 데이터 소스에서 들어오는 ID를 필터링하고 ID만 전달하도록 허용합니다.

   ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]. Audience Manager UI에서 대상을 만들 때 이 옵션을 선택합니다. 먼저 [!UICONTROL Inbound] 을 선택한 다음 원하는 ID 유형을 선택합니다. 옵션은 다음과 같습니다.

   ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]. 이 옵션은 내보낼 파일 형식을 결정합니다. **[!UICONTROL Add Destination]** 워크플로우의 **[!UICONTROL Batch Data]**&#x200B;에서 형식을 선택합니다.

형식을 검사하려면 **[!UICONTROL Admin UI > Formats]**(으)로 이동하여 [!UICONTROL Data Row] 요소를 찾습니다. 이 요소에는 아래 예에서 파일 형식 &lt;MCID>의 매크로가 포함되어 있습니다.

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 구성 번호. </th> 
   <th colname="col1" class="entry"> <p>사용자 키 </p> </th> 
   <th colname="col2" class="entry"> <p>데이터 소스 유형 </p> </th> 
   <th colname="col3" class="entry"> <p>형식 </p> </th> 
   <th colname="col4" class="entry"> <p>내보낸 ID 유형 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>고객 ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>고객 ID(DPUUID) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>고객 ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>고객 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;dp_uuid&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID(회사에서 액세스할 수 있는 모든 데이터 소스) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## 사용 사례

Audience Manager 및 [!DNL Campaign]을 사용한다고 가정해 보겠습니다. [!DNL Campaign]에서 고객 데이터를 실행 가능하게 하려면 [!UICONTROL Experience Cloud IDs]을(를) 내보내려고 합니다. 이 경우 구성 번호 3을 사용해야 합니다.
