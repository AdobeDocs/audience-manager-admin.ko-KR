---
description: 일부 고객은 버킷에 대상 데이터 업로드를 인증하기 위해 Adobe에 대한 Amazon 단순 스토리지 서비스(Amazon S3) 액세스 또는 비밀 키를 제공하지 않으려는 경우가 있습니다.
seo-description: 일부 고객은 버킷에 대상 데이터 업로드를 인증하기 위해 Adobe에 대한 Amazon 단순 스토리지 서비스(Amazon S3) 액세스 또는 비밀 키를 제공하지 않으려는 경우가 있습니다.
seo-title: 배치 대상에 대한 교차 계정 Amazon S3 버켓 액세스를 인증하는 방법
title: 배치 대상에 대한 교차 계정 Amazon S3 버켓 액세스를 인증하는 방법
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# 배치 대상에 대한 교차 계정 Amazon S3 버킷 액세스를 인증하는 방법{#authorize-cross-account-bucket-batch}

일부 고객은 자신의 버킷에 대상 데이터 업로드를 인증하기 위해 Adobe에 [!DNL Amazon S3] 액세스 또는 비밀 키를 제공하지 않을 수도 있습니다.

고객에게 제공할 수 있는 대체 방법은 [!DNL Amazon S3]의 [!UICONTROL Cross-Account Bucket Permissions]입니다. 이 프로세스는 [AWS 설명서](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)에 설명되어 있습니다. Audience Manager에서 이 대체 요소를 활성화하려면 아래 단계를 수행하십시오.

1. **[!UICONTROL Servers]**&#x200B;으로 이동하고 **[!UICONTROL Create Server]**&#x200B;을 선택합니다.
1. **[!UICONTROL Protocol/Credentials]** 드롭다운 마스크에서 **[!UICONTROL S3]**&#x200B;을 선택합니다.
1. **[!UICONTROL Use Internal Adobe Key]** 옵션을 선택합니다.
1. [!DNL Amazon S3]에서 고객의 계정과 버킷 이름을 사용하십시오.
1. 고객 화이트리스트에 [!DNL S3] 버킷에 [!DNL Amazon S3] 계정 `975822914085`이 표시되는지 확인하십시오.

>[!NOTE]
>
>아웃바운드 게시자는 고객이 해당 데이터를 소유할 수 있도록 권한 수준 `bucket-owner-full-control`이 업로드된 데이터에 설정되어 있는지 확인합니다.
