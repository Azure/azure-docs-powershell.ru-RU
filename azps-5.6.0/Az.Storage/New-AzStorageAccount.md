---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993205"
---
# <span data-ttu-id="0fc83-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0fc83-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="0fc83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fc83-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc83-103">Создает учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="0fc83-103">Creates a Storage account.</span></span>

## <span data-ttu-id="0fc83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0fc83-104">SYNTAX</span></span>

### <span data-ttu-id="0fc83-105">AzureActiveDirectoryDomainServicesForFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0fc83-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="0fc83-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="0fc83-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="0fc83-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fc83-107">DESCRIPTION</span></span>
<span data-ttu-id="0fc83-108">С **его учетной записью создается** учетная запись хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0fc83-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="0fc83-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0fc83-109">EXAMPLES</span></span>

### <span data-ttu-id="0fc83-110">Пример 1. Создание учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="0fc83-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="0fc83-111">Эта команда создает учетную запись хранения для группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0fc83-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="0fc83-112">Пример 2. Создание учетной записи хранилища BLOB-хранилищ с помощью BlobStorage Kind и hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="0fc83-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="0fc83-113">Эта команда создает учетную запись хранилища BLOB-хранилищ, которая с BlobStorage Kind и hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="0fc83-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="0fc83-114">Пример 3. Создайте учетную запись хранения с помощью Kind StorageV2 и создайте и назначьте удостоверение для Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0fc83-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="0fc83-115">Эта команда создает учетную запись хранения с kind StorageV2.</span><span class="sxs-lookup"><span data-stu-id="0fc83-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="0fc83-116">Кроме того, оно создает и назначает удостоверение, которое можно использовать для управления ключами учетных записей с помощью ключей Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0fc83-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="0fc83-117">Пример 4. Создание учетной записи хранения с помощью NetworkRuleSet из JSON</span><span class="sxs-lookup"><span data-stu-id="0fc83-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="0fc83-118">Эта команда создает учетную запись хранения с свойством NetworkRuleSet из JSON.</span><span class="sxs-lookup"><span data-stu-id="0fc83-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="0fc83-119">Пример 5. Создание учетной записи хранения с включенной иерархической областью имен.</span><span class="sxs-lookup"><span data-stu-id="0fc83-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="0fc83-120">Эта команда создает учетную запись хранения с включенной иерархической областью имен.</span><span class="sxs-lookup"><span data-stu-id="0fc83-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="0fc83-121">Пример 6. Создание учетной записи хранения с помощью проверки подлинности AAD DS Azure и использование большой папки с файлами.</span><span class="sxs-lookup"><span data-stu-id="0fc83-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="0fc83-122">Эта команда создает учетную запись хранения с проверкой подлинности AAD DS Azure и включает большой объем файловой папки.</span><span class="sxs-lookup"><span data-stu-id="0fc83-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="0fc83-123">Пример 7. Создание учетной записи хранения с возможностью проверки подлинности доменной службы Files Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0fc83-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="0fc83-124">Эта команда создает учетную запись хранения с проверкой подлинности доменной службы Active Directory "Файлы Active Directory".</span><span class="sxs-lookup"><span data-stu-id="0fc83-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="0fc83-125">Пример 8. Создайте учетную запись хранения с помощью очереди и службы таблиц с помощью ключа шифрования уровня учетной записи и обязательного шифрования инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="0fc83-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

<span data-ttu-id="0fc83-126">Эта команда создает учетную запись хранения с очереди, а табличные службы используют ключ шифрования уровня учетной записи и требуют шифрования инфраструктуры, поэтому для очереди и таблицы будет применяться один и тот же ключ шифрования для BLOB-объектов и файловой службы, а служба приместит дополнительный уровень шифрования с управляемыми платформой ключами для неавторятельных данных.</span><span class="sxs-lookup"><span data-stu-id="0fc83-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="0fc83-127">Затем получите свойства учетной записи хранения и просмотреть тип ключа шифрования очереди и табличная служба и значение RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="0fc83-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="0fc83-128">Пример 9. Создание учетной записи MinimumTlsVersion и AllowBlobPublicAccess и отключение Доступа SharedKey</span><span class="sxs-lookup"><span data-stu-id="0fc83-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess, and disable SharedKey Access</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

<span data-ttu-id="0fc83-129">Команда для создания учетной записи MinimumTlsVersion, AllowBlobPublicAccess и отключения доступа SharedKey к учетной записи, а затем показать три свойства созданной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="0fc83-129">The command create account with MinimumTlsVersion, AllowBlobPublicAccess, and disable SharedKey access to the account, and then show the the 3 properties of the created account</span></span> 

### <span data-ttu-id="0fc83-130">Пример 10. Создание учетной записи хранения с параметром RoutingPreference</span><span class="sxs-lookup"><span data-stu-id="0fc83-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="0fc83-131">Эта команда создает учетную запись хранения с параметром RoutingPreference: PublishMicrosoftEndpoint и PublishInternetEndpoint как true, и RoutingChoice как MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="0fc83-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="0fc83-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fc83-132">PARAMETERS</span></span>

### <span data-ttu-id="0fc83-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="0fc83-133">-AccessTier</span></span>
<span data-ttu-id="0fc83-134">Определяет уровень доступа к учетной записи хранения, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fc83-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="0fc83-135">Допустимыми значениями для этого параметра являются hot и Cool.</span><span class="sxs-lookup"><span data-stu-id="0fc83-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="0fc83-136">Если для параметра *Kind* указано значение BlobStorage, необходимо указать значение *параметра AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="0fc83-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="0fc83-137">Если для этого параметра Kind задан параметр *Storage,* не укажите параметр *AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="0fc83-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="0fc83-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="0fc83-139">Определяет идентификатор безопасности для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0fc83-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="0fc83-140">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="0fc83-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="0fc83-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="0fc83-142">Определяет GUID домена.</span><span class="sxs-lookup"><span data-stu-id="0fc83-142">Specifies the domain GUID.</span></span> <span data-ttu-id="0fc83-143">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="0fc83-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="0fc83-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="0fc83-145">Определяет основной домен, для который является полномочного DNS-сервером AD.</span><span class="sxs-lookup"><span data-stu-id="0fc83-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="0fc83-146">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="0fc83-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="0fc83-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="0fc83-148">Идентификатор безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="0fc83-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="0fc83-149">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="0fc83-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="0fc83-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="0fc83-151">Указывает лес Active Directory, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="0fc83-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="0fc83-152">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="0fc83-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-153">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="0fc83-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="0fc83-154">Указывает доменное имя NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="0fc83-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="0fc83-155">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="0fc83-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-156">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="0fc83-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="0fc83-157">Разрешить общедоступный доступ ко всем BLOB-контейнерам в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0fc83-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="0fc83-158">Для этого свойства по умолчанию верно верное толкование.</span><span class="sxs-lookup"><span data-stu-id="0fc83-158">The default interpretation is true for this property.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-159">-AllowSharedKeyAccess</span><span class="sxs-lookup"><span data-stu-id="0fc83-159">-AllowSharedKeyAccess</span></span>
<span data-ttu-id="0fc83-160">Указывает, разрешено ли учетной записи хранения запрашивать разрешение с помощью ключа доступа учетной записи с помощью общего ключа.</span><span class="sxs-lookup"><span data-stu-id="0fc83-160">Indicates whether the storage account permits requests to be authorized with the account access key via Shared Key.</span></span> <span data-ttu-id="0fc83-161">Если это так, все запросы, включая подписи общего доступа, должны быть авторизованны в Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="0fc83-161">If false, then all requests, including shared access signatures, must be authorized with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="0fc83-162">Значение по умолчанию равно NULL, что эквивалентно значению ИСТИНА.</span><span class="sxs-lookup"><span data-stu-id="0fc83-162">The default value is null, which is equivalent to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-163">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fc83-163">-AsJob</span></span>
<span data-ttu-id="0fc83-164">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0fc83-164">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-165">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0fc83-165">-AssignIdentity</span></span>
<span data-ttu-id="0fc83-166">Создание и назначение удостоверения учетной записи хранения для этой учетной записи хранения для использования с основными службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0fc83-166">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-167">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="0fc83-167">-CustomDomainName</span></span>
<span data-ttu-id="0fc83-168">Указывает имя пользовательского домена учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0fc83-168">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="0fc83-169">Значение по умолчанию — "Хранилище".</span><span class="sxs-lookup"><span data-stu-id="0fc83-169">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc83-170">-DefaultProfile</span></span>
<span data-ttu-id="0fc83-171">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fc83-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="0fc83-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="0fc83-173">В этой службе можно включить проверку подлинности доменной службы Azure Files Active Directory для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0fc83-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="0fc83-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="0fc83-175">В этой области можно включить проверку подлинности доменной службы Azure Active Directory для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0fc83-175">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-176">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="0fc83-176">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="0fc83-177">Указывает, включает ли учетная запись хранения иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="0fc83-177">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="0fc83-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="0fc83-179">Указывает, включает ли учетная запись хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0fc83-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="0fc83-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="0fc83-181">Указывает, поддерживает ли учетная запись хранения большие папки емкостью более 5 ТБ.</span><span class="sxs-lookup"><span data-stu-id="0fc83-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="0fc83-182">После включения учетной записи эту функцию невозможно отключить.</span><span class="sxs-lookup"><span data-stu-id="0fc83-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="0fc83-183">В настоящее время поддерживается только для типов репликации LRS и ZRS, поэтому преобразование учетных записей в геоизбыточные учетные записи невозможно.</span><span class="sxs-lookup"><span data-stu-id="0fc83-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="0fc83-184">Подробнее в https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="0fc83-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-185">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="0fc83-185">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="0fc83-186">За установите keyType шифрования для очереди.</span><span class="sxs-lookup"><span data-stu-id="0fc83-186">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="0fc83-187">Значение по умолчанию — Service (Служба).</span><span class="sxs-lookup"><span data-stu-id="0fc83-187">The default value is Service.</span></span>
<span data-ttu-id="0fc83-188">-Account: Очередь шифруется с помощью ключа шифрования уровня учетной записи.</span><span class="sxs-lookup"><span data-stu-id="0fc83-188">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="0fc83-189">-Service: Очередь всегда шифруется с помощью Service-Managed клавиш.</span><span class="sxs-lookup"><span data-stu-id="0fc83-189">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-190">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="0fc83-190">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="0fc83-191">За установите ключ шифрования для таблицы.</span><span class="sxs-lookup"><span data-stu-id="0fc83-191">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="0fc83-192">Значение по умолчанию — Service (Служба).</span><span class="sxs-lookup"><span data-stu-id="0fc83-192">The default value is Service.</span></span>
- <span data-ttu-id="0fc83-193">Учетная запись: таблица будет зашифрована с помощью ключа шифрования уровня учетной записи.</span><span class="sxs-lookup"><span data-stu-id="0fc83-193">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="0fc83-194">Служба: таблица всегда шифруется с Service-Managed клавиш.</span><span class="sxs-lookup"><span data-stu-id="0fc83-194">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-195">-Kind</span><span class="sxs-lookup"><span data-stu-id="0fc83-195">-Kind</span></span>
<span data-ttu-id="0fc83-196">Определяет тип учетной записи хранения, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fc83-196">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="0fc83-197">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="0fc83-197">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0fc83-198">"Хранилище".</span><span class="sxs-lookup"><span data-stu-id="0fc83-198">Storage.</span></span> <span data-ttu-id="0fc83-199">Учетная запись хранения общего назначения, которая поддерживает хранение BLOB-файлов, таблиц, очередей, файлов и дисков.</span><span class="sxs-lookup"><span data-stu-id="0fc83-199">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="0fc83-200">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="0fc83-200">StorageV2.</span></span> <span data-ttu-id="0fc83-201">Учетная запись хранения общего назначения версии 2 (GPv2), которая поддерживает большие объекты, таблицы, очереди, файлы и диски, с расширенными возможностями, например переучетом данных.</span><span class="sxs-lookup"><span data-stu-id="0fc83-201">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="0fc83-202">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="0fc83-202">BlobStorage.</span></span> <span data-ttu-id="0fc83-203">Учетная запись хранилища BLOB-хранилищ, которая поддерживает хранение только BLOB-хранилищ.</span><span class="sxs-lookup"><span data-stu-id="0fc83-203">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="0fc83-204">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="0fc83-204">BlockBlobStorage.</span></span> <span data-ttu-id="0fc83-205">Блокировать учетную запись хранилища BLOB-блоков, которая поддерживает только хранение блоков BLOB-блоков.</span><span class="sxs-lookup"><span data-stu-id="0fc83-205">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="0fc83-206">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="0fc83-206">FileStorage.</span></span> <span data-ttu-id="0fc83-207">Учетная запись хранилища файлов, которая поддерживает только хранение файлов.</span><span class="sxs-lookup"><span data-stu-id="0fc83-207">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="0fc83-208">Значение по умолчанию — StorageV2.</span><span class="sxs-lookup"><span data-stu-id="0fc83-208">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-209">-Location</span><span class="sxs-lookup"><span data-stu-id="0fc83-209">-Location</span></span>
<span data-ttu-id="0fc83-210">Определяет расположение создаемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0fc83-210">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-211">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0fc83-211">-MinimumTlsVersion</span></span>
<span data-ttu-id="0fc83-212">Минимальная версия TLS, разрешенная для запросов на хранение.</span><span class="sxs-lookup"><span data-stu-id="0fc83-212">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="0fc83-213">По умолчанию для этого свойства зачитуется значение TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="0fc83-213">The default interpretation is TLS 1.0 for this property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-214">-Name</span><span class="sxs-lookup"><span data-stu-id="0fc83-214">-Name</span></span>
<span data-ttu-id="0fc83-215">Имя создаемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0fc83-215">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-216">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0fc83-216">-NetworkRuleSet</span></span>
<span data-ttu-id="0fc83-217">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для определения значений сетевых свойств, таких как службы, разрешенные для обхода правил, и обработки запросов, которые не соответствуют ни одной из них.</span><span class="sxs-lookup"><span data-stu-id="0fc83-217">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-218">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="0fc83-218">-PublishInternetEndpoint</span></span>
<span data-ttu-id="0fc83-219">Указывает на то, должны ли публиковаться конечные точки для хранения маршрутов в Интернете.</span><span class="sxs-lookup"><span data-stu-id="0fc83-219">Indicates whether internet  routing storage endpoints are to be published</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-220">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="0fc83-220">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="0fc83-221">Указывает на то, должны ли публиковаться конечные точки хранилища маршрутов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0fc83-221">Indicates whether microsoft routing storage endpoints are to be published</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-222">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="0fc83-222">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="0fc83-223">Служба будет применять дополнительный уровень шифрования с управляемыми платформой ключами для неавторяых данных.</span><span class="sxs-lookup"><span data-stu-id="0fc83-223">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-224">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc83-224">-ResourceGroupName</span></span>
<span data-ttu-id="0fc83-225">Имя группы ресурсов, в которую нужно добавить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="0fc83-225">Specifies the name of the resource group in which to add the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-226">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="0fc83-226">-RoutingChoice</span></span>
<span data-ttu-id="0fc83-227">Выбор маршрутии определяет тип сетевой маршрутии, opted пользователем.</span><span class="sxs-lookup"><span data-stu-id="0fc83-227">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="0fc83-228">Возможные значения: "MicrosoftRouting", "InternetRouting"</span><span class="sxs-lookup"><span data-stu-id="0fc83-228">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-229">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0fc83-229">-SkuName</span></span>
<span data-ttu-id="0fc83-230">Указывает имя SKU учетной записи хранения, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fc83-230">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="0fc83-231">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="0fc83-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0fc83-232">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="0fc83-232">Standard_LRS.</span></span> <span data-ttu-id="0fc83-233">Локальное избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="0fc83-233">Locally-redundant storage.</span></span>
- <span data-ttu-id="0fc83-234">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="0fc83-234">Standard_ZRS.</span></span> <span data-ttu-id="0fc83-235">Избыточное хранилище зоны.</span><span class="sxs-lookup"><span data-stu-id="0fc83-235">Zone-redundant storage.</span></span>
- <span data-ttu-id="0fc83-236">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="0fc83-236">Standard_GRS.</span></span> <span data-ttu-id="0fc83-237">Гео избыточный объем хранилища.</span><span class="sxs-lookup"><span data-stu-id="0fc83-237">Geo-redundant storage.</span></span>
- <span data-ttu-id="0fc83-238">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="0fc83-238">Standard_RAGRS.</span></span> <span data-ttu-id="0fc83-239">Чтение геобытного хранилища в Access.</span><span class="sxs-lookup"><span data-stu-id="0fc83-239">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="0fc83-240">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="0fc83-240">Premium_LRS.</span></span> <span data-ttu-id="0fc83-241">"Премиум" — локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="0fc83-241">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="0fc83-242">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="0fc83-242">Premium_ZRS.</span></span> <span data-ttu-id="0fc83-243">Premium zone-redundant storage.</span><span class="sxs-lookup"><span data-stu-id="0fc83-243">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="0fc83-244">Standard_GZRS — гео-избыточное хранилище зоны— избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="0fc83-244">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="0fc83-245">Standard_RAGZRS — чтение доступа к гео-избыточной зоне, избыточный объем хранилища.</span><span class="sxs-lookup"><span data-stu-id="0fc83-245">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-246">-Tag</span><span class="sxs-lookup"><span data-stu-id="0fc83-246">-Tag</span></span>
<span data-ttu-id="0fc83-247">Пары значений ключа в виде hash table set as tags (Теги на сервере).</span><span class="sxs-lookup"><span data-stu-id="0fc83-247">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="0fc83-248">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0fc83-248">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-249">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="0fc83-249">-UseSubDomain</span></span>
<span data-ttu-id="0fc83-250">Указывает, следует ли включить непрямую проверку CName.</span><span class="sxs-lookup"><span data-stu-id="0fc83-250">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fc83-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc83-251">CommonParameters</span></span>
<span data-ttu-id="0fc83-252">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fc83-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc83-253">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fc83-253">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc83-254">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fc83-254">INPUTS</span></span>

### <span data-ttu-id="0fc83-255">System.String</span><span class="sxs-lookup"><span data-stu-id="0fc83-255">System.String</span></span>

## <span data-ttu-id="0fc83-256">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0fc83-256">OUTPUTS</span></span>

### <span data-ttu-id="0fc83-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0fc83-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0fc83-258">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0fc83-258">NOTES</span></span>

## <span data-ttu-id="0fc83-259">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fc83-259">RELATED LINKS</span></span>

[<span data-ttu-id="0fc83-260">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0fc83-260">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="0fc83-261">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0fc83-261">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="0fc83-262">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0fc83-262">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
