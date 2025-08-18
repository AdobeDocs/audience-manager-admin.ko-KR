---
description: Audience Manager 관리 도구의 서버 페이지를 사용하여 새 FTP 서버를 만들거나 기존 서버를 편집합니다.
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: FTP 서버 만들기 또는 편집
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 8af040e49b881302315e0b66baa73db47c5eee28
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 1%

---

# FTP 서버 만들기 또는 편집 {#create-or-edit-an-ftp-server}

Audience Manager 관리 도구의 [!UICONTROL Servers] 페이지를 사용하여 새 FTP 서버를 만들거나 기존 서버를 편집합니다.

>[!NOTE]
>
>새 서버를 만들거나 기존 서버를 편집하려면 [!UICONTROL DEXADMIN] 역할이 있어야 합니다.

1. 새 서버를 만들려면 **[!UICONTROL Servers]** > **[!UICONTROL Create Server]**&#x200B;을(를) 클릭합니다. 기존 서버를 편집하려면 **[!UICONTROL Label]** 열에서 원하는 서버를 클릭합니다.
1. 이 서버에 대해 원하는 레이블을 지정합니다.
1. **[!UICONTROL Protocol]** 드롭다운 목록에서 원하는 프로토콜을 선택합니다. **FTP**.

   >[!NOTE]
   >
   >가장 좋은 방법은 [!DNL Amazon S3]을(를) 사용하여 파트너로부터 파일을 가져오고 파트너에게 파일을 전달하는 것입니다. [!DNL Amazon S3]은(는) 웹 상의 어디에서나 언제든지 원하는 양의 데이터를 저장하고 검색하는 데 사용할 수 있는 간단한 웹 서비스 인터페이스를 제공합니다. 자세한 내용은 [Amazon 사용 안내서](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html)의 *Audience Manager S3 정보*&#x200B;를 참조하십시오.

1. 다음 필드를 채웁니다.

   * **[!UICONTROL Type]:** 원하는 암호화 유형: **[!UICONTROL SFTP]** 또는 **[!UICONTROL FTPs/TLS]**&#x200B;을(를) 선택합니다.
   * **[!UICONTROL Domain]:** 이 서버에 대해 원하는 도메인(호스트)을 지정하십시오.
   * **[!UICONTROL Port]:** 이 서버에 대해 원하는 포트를 지정하십시오. 기본 포트는 각 암호화 유형에 대해 표시됩니다. 필요한 경우 기본 포트를 변경할 수 있습니다.
   * **[!UICONTROL Remote Path]:** 이 서버에 대해 원하는 원격 경로를 지정하십시오. 이 필드를 비워 두면 Audience Manager은 파일을 기본 디렉터리에 배치합니다.
   * **[!UICONTROL .tmp File Rename on Completion]:** 이 옵션을 사용하면 완료 시 `.tmp` 파일의 이름을 바꿀 수 있습니다.
   * **[!UICONTROL Filename Suffix]:** 파일을 전송할 텍스트를 지정합니다.
   * **[!UICONTROL Moved to When Finished]:** 완료 시 전송 파일을 이동할 위치에 대한 경로를 지정합니다.
   * **[!UICONTROL Authentication]:** 원하는 서버 인증 방법: **[!UICONTROL Username/Password]** 또는 **[!UICONTROL SSH Key]**&#x200B;을(를) 지정합니다.

   >[!NOTE]
   >
   >허용 IP 목록: [!DNL FTP]에 이그레스 [!DNL IP] **54.204.116.43**&#x200B;을(를) 추가해야 합니다.

1. **[!UICONTROL SSH Key]** 인증:
   >[!NOTE]
   >
   >SSH 키 인증을 구성할 때는 항상 OpenSSH 형식으로만 공개 및 개인 키를 생성해야 합니다.
   1. [!DNL Linux] 또는 [!DNL Mac] 컴퓨터에서 공개/개인 키 쌍을 생성합니다.
   1. 클라이언트에 **공개 키**&#x200B;을(를) 제공하여 [!DNL SFTP] 서버에서 업데이트합니다. `-----BEGIN RSA PRIVATE KEY-----` 및 `-----END RSA PRIVATE KEY-----` 등 서버의 공개 키에 있는 모든 텍스트를 포함해야 합니다. 대신 키를 설치할 사용자 이름을 제공해야 합니다.
   1. 사용자 이름 필드를 클라이언트가 제공한 값으로 업데이트하고 키 필드를 **개인 키**(으)로 업데이트합니다.
1. 새 서버를 만드는 경우 **[!UICONTROL Create]**&#x200B;을(를) 클릭하고 기존 서버를 편집하는 경우 **[!UICONTROL Update]**&#x200B;을(를) 클릭합니다.
