---
description: 일부 고객은 버킷에 대한 대상 데이터 업로드를 승인하기 위해 Amazon Simple Storage Service(Amazon S3) 액세스 또는 Adobe에 비밀 키를 제공하지 않을 수 있습니다.
seo-description: Some customers may not want to provide their Amazon Simple Storage Service (Amazon S3) access or secret keys to Adobe to authorize destination data upload to their buckets.
seo-title: How To  Authorize Cross-Account Amazon S3 Bucket Access for Batch Destinations
title: 배치 대상에 대한 교차 계정 Amazon S3 버킷 액세스 권한을 부여하는 방법
uuid: da2bcbda-a765-437a-bfe9-4355383a4730
exl-id: f3b97c31-714f-4841-884b-bc507267a932
TQID: https://experienceleague.adobe.com/KFc06xetyatq5n-F8Uu-6nmepyjbFyQ3nYB-vXkdPdE
product_v2: id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2: id: c814092e-2730-45e8-a12d-e084529f52cb
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 0%

---

# 배치 대상에 대한 교차 계정 Amazon S3 버킷 액세스 권한을 부여하는 방법{#authorize-cross-account-bucket-batch}

일부 고객은 버킷에 대한 대상 데이터 업로드를 승인하기 위해 Adobe에 대한 [!DNL Amazon S3] 액세스 또는 비밀 키를 제공하지 않을 수 있습니다.

고객에게 제공할 수 있는 대안은 [!DNL Amazon S3]의 [!UICONTROL Cross-Account Bucket Permissions]입니다. 이 프로세스는 [AWS 설명서](https://docs.aws.amazon.com/AmazonS3/latest/dev/example-walkthroughs-managing-access-example2.html)에 설명되어 있습니다. Audience Manager에서 이 대체 요소를 활성화하려면 아래 단계를 따르십시오.

1. **[!UICONTROL Servers]**(으)로 이동하여 **[!UICONTROL Create Server]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Protocol/Credentials]** 드롭다운 마스크에서 **[!UICONTROL S3]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Use Internal Adobe Key]** 옵션을 선택하십시오.
1. [!DNL Amazon S3]에서 고객의 계정과 버킷 이름을 사용하십시오.
1. 고객의 [!DNL S3] 버킷에 [!DNL Amazon S3] 계정 `975822914085`이(가) 나열되어 있는지 확인하십시오.

>[!NOTE]
>
>아웃바운드 게시자는 고객이 해당 데이터를 소유할 수 있도록 업로드된 데이터에 대한 권한 수준 `bucket-owner-full-control`을(를) 설정합니다.
