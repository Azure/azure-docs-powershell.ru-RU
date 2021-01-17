---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324845"
---
# <span data-ttu-id="52d3e-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52d3e-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="52d3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="52d3e-103">Создает учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="52d3e-103">Creates a Storage account.</span></span>

## <span data-ttu-id="52d3e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="52d3e-104">SYNTAX</span></span>

### <span data-ttu-id="52d3e-105">AzureActiveDirectoryDomainServicesForFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52d3e-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52d3e-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="52d3e-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52d3e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52d3e-107">DESCRIPTION</span></span>
<span data-ttu-id="52d3e-108">С **его учетной записью создается** учетная запись хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="52d3e-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="52d3e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="52d3e-109">EXAMPLES</span></span>

### <span data-ttu-id="52d3e-110">Пример 1. Создание учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="52d3e-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="52d3e-111">Эта команда создает учетную запись хранения для группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="52d3e-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="52d3e-112">Пример 2. Создание учетной записи хранилища BLOB-хранилищ с помощью BlobStorage Kind и hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="52d3e-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="52d3e-113">Эта команда создает учетную запись хранилища BLOB-хранилищ, которая с BlobStorage Kind и hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="52d3e-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="52d3e-114">Пример 3. Создайте учетную запись хранения с помощью Kind StorageV2 и создайте и назначьте удостоверение для Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="52d3e-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="52d3e-115">Эта команда создает учетную запись хранения с kind StorageV2.</span><span class="sxs-lookup"><span data-stu-id="52d3e-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="52d3e-116">Кроме того, оно создает и назначает удостоверение, которое можно использовать для управления ключами учетных записей с помощью ключей Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="52d3e-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="52d3e-117">Пример 4. Создание учетной записи хранения с помощью NetworkRuleSet из JSON</span><span class="sxs-lookup"><span data-stu-id="52d3e-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="52d3e-118">Эта команда создает учетную запись хранения с свойством NetworkRuleSet из JSON.</span><span class="sxs-lookup"><span data-stu-id="52d3e-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="52d3e-119">Пример 5. Создание учетной записи хранения с включенной иерархической областью имен.</span><span class="sxs-lookup"><span data-stu-id="52d3e-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="52d3e-120">Эта команда создает учетную запись хранения с включенной иерархической областью имен.</span><span class="sxs-lookup"><span data-stu-id="52d3e-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="52d3e-121">Пример 6. Создание учетной записи хранения с помощью проверки подлинности AAD DS Azure и использование большой папки с файлами.</span><span class="sxs-lookup"><span data-stu-id="52d3e-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="52d3e-122">Эта команда создает учетную запись хранения с проверкой подлинности azure Files AAD DS и включает большой объем файловой папки.</span><span class="sxs-lookup"><span data-stu-id="52d3e-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="52d3e-123">Пример 7. Создайте учетную запись хранения с возможностью проверки подлинности доменной службы Files Active Directory.</span><span class="sxs-lookup"><span data-stu-id="52d3e-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="52d3e-124">Эта команда создает учетную запись хранения с проверкой подлинности доменной службы Active Directory "Файлы Active Directory".</span><span class="sxs-lookup"><span data-stu-id="52d3e-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="52d3e-125">Пример 8. Создайте учетную запись хранения с помощью очереди и службы таблиц с помощью ключа шифрования уровня учетной записи и обязательного шифрования инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="52d3e-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="52d3e-126">Эта команда создает учетную запись хранения с очереди, а табличные службы используют ключ шифрования уровня учетной записи и требуют шифрования инфраструктуры, поэтому для очереди и таблицы будет применяться один и тот же ключ шифрования для BLOB-объектов и файловой службы, а служба приместит дополнительный уровень шифрования с управляемыми платформой ключами для неавторятельных данных.</span><span class="sxs-lookup"><span data-stu-id="52d3e-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="52d3e-127">Затем получите свойства учетной записи хранения и просмотреть тип ключа шифрования очереди и табличная служба и значение RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="52d3e-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="52d3e-128">Пример 9. Создание учетной записи MinimumTlsVersion и AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="52d3e-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="52d3e-129">Команда для создания учетной записи с minimumTlsVersion и AllowBlobPublicAccess, а затем показать 2 свойства созданной учетной записи</span><span class="sxs-lookup"><span data-stu-id="52d3e-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="52d3e-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52d3e-130">PARAMETERS</span></span>

### <span data-ttu-id="52d3e-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="52d3e-131">-AccessTier</span></span>
<span data-ttu-id="52d3e-132">Определяет уровень доступа к учетной записи хранения, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52d3e-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="52d3e-133">Допустимыми значениями для этого параметра являются hot и Cool.</span><span class="sxs-lookup"><span data-stu-id="52d3e-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="52d3e-134">Если для параметра *Kind* указано значение BlobStorage, необходимо указать значение *параметра AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="52d3e-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="52d3e-135">Если для этого параметра Kind задан параметр *Storage,* не укажите параметр *AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="52d3e-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="52d3e-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="52d3e-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="52d3e-137">Определяет идентификатор безопасности для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="52d3e-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="52d3e-138">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="52d3e-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="52d3e-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="52d3e-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="52d3e-140">Определяет GUID домена.</span><span class="sxs-lookup"><span data-stu-id="52d3e-140">Specifies the domain GUID.</span></span> <span data-ttu-id="52d3e-141">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="52d3e-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="52d3e-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="52d3e-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="52d3e-143">Определяет основной домен, для который является полномочного DNS-сервером AD.</span><span class="sxs-lookup"><span data-stu-id="52d3e-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="52d3e-144">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="52d3e-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="52d3e-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="52d3e-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="52d3e-146">Идентификатор безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="52d3e-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="52d3e-147">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="52d3e-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="52d3e-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="52d3e-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="52d3e-149">Указывает лес Active Directory, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="52d3e-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="52d3e-150">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="52d3e-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="52d3e-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="52d3e-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="52d3e-152">Указывает доменное имя NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="52d3e-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="52d3e-153">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="52d3e-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="52d3e-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="52d3e-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="52d3e-155">Разрешить общедоступный доступ ко всем BLOB-контейнерам в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="52d3e-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="52d3e-156">Для этого свойства по умолчанию верно верное толкование.</span><span class="sxs-lookup"><span data-stu-id="52d3e-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="52d3e-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52d3e-157">-AsJob</span></span>
<span data-ttu-id="52d3e-158">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="52d3e-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52d3e-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="52d3e-159">-AssignIdentity</span></span>
<span data-ttu-id="52d3e-160">Создание и назначение удостоверения учетной записи хранения для этой учетной записи хранения для использования с основными службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="52d3e-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="52d3e-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="52d3e-161">-CustomDomainName</span></span>
<span data-ttu-id="52d3e-162">Указывает имя пользовательского домена учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="52d3e-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="52d3e-163">Значение по умолчанию — "Хранилище".</span><span class="sxs-lookup"><span data-stu-id="52d3e-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="52d3e-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d3e-164">-DefaultProfile</span></span>
<span data-ttu-id="52d3e-165">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52d3e-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52d3e-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="52d3e-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="52d3e-167">В этой службе можно включить проверку подлинности доменной службы Azure Files Active Directory для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="52d3e-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="52d3e-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="52d3e-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="52d3e-169">В этой области можно включить проверку подлинности доменной службы Azure Active Directory для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="52d3e-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="52d3e-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="52d3e-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="52d3e-171">Указывает, включает ли учетная запись хранения иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="52d3e-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="52d3e-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="52d3e-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="52d3e-173">Указывает, включает ли учетная запись хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="52d3e-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="52d3e-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="52d3e-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="52d3e-175">Указывает, поддерживает ли учетная запись хранения большие папки емкостью более 5 ТБ.</span><span class="sxs-lookup"><span data-stu-id="52d3e-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="52d3e-176">После включения учетной записи эту функцию невозможно отключить.</span><span class="sxs-lookup"><span data-stu-id="52d3e-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="52d3e-177">В настоящее время поддерживается только для типов репликации LRS и ZRS, поэтому преобразование учетных записей в геоизбыточные учетные записи невозможно.</span><span class="sxs-lookup"><span data-stu-id="52d3e-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="52d3e-178">Подробнее в https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="52d3e-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="52d3e-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="52d3e-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="52d3e-180">За установите keyType шифрования для очереди.</span><span class="sxs-lookup"><span data-stu-id="52d3e-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="52d3e-181">Значение по умолчанию — Service (Служба).</span><span class="sxs-lookup"><span data-stu-id="52d3e-181">The default value is Service.</span></span>
<span data-ttu-id="52d3e-182">-Account: Очередь шифруется с помощью ключа шифрования на уровнях учетной записи.</span><span class="sxs-lookup"><span data-stu-id="52d3e-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="52d3e-183">-Service: Очередь всегда шифруется с Service-Managed клавиш.</span><span class="sxs-lookup"><span data-stu-id="52d3e-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="52d3e-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="52d3e-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="52d3e-185">За установите ключ шифрования для таблицы.</span><span class="sxs-lookup"><span data-stu-id="52d3e-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="52d3e-186">Значение по умолчанию — Service (Служба).</span><span class="sxs-lookup"><span data-stu-id="52d3e-186">The default value is Service.</span></span>
- <span data-ttu-id="52d3e-187">Учетная запись: таблица будет зашифрована с помощью ключа шифрования уровня учетной записи.</span><span class="sxs-lookup"><span data-stu-id="52d3e-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="52d3e-188">Служба: таблица всегда шифруется с Service-Managed клавиш.</span><span class="sxs-lookup"><span data-stu-id="52d3e-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="52d3e-189">-Kind</span><span class="sxs-lookup"><span data-stu-id="52d3e-189">-Kind</span></span>
<span data-ttu-id="52d3e-190">Определяет тип учетной записи хранения, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52d3e-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="52d3e-191">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="52d3e-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52d3e-192">"Хранилище".</span><span class="sxs-lookup"><span data-stu-id="52d3e-192">Storage.</span></span> <span data-ttu-id="52d3e-193">Учетная запись хранения общего назначения, которая поддерживает хранение BLOB-файлов, таблиц, очередей, файлов и дисков.</span><span class="sxs-lookup"><span data-stu-id="52d3e-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="52d3e-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="52d3e-194">StorageV2.</span></span> <span data-ttu-id="52d3e-195">Учетная запись хранения общего назначения версии 2 (GPv2), которая поддерживает большие большие объекты, таблицы, очереди, файлы и диски, с расширенными возможностями, например переучетом данных.</span><span class="sxs-lookup"><span data-stu-id="52d3e-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="52d3e-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="52d3e-196">BlobStorage.</span></span> <span data-ttu-id="52d3e-197">Учетная запись хранилища BLOB-хранилищ, которая поддерживает хранение только BLOB-хранилищ.</span><span class="sxs-lookup"><span data-stu-id="52d3e-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="52d3e-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="52d3e-198">BlockBlobStorage.</span></span> <span data-ttu-id="52d3e-199">Блокировать учетную запись хранилища BLOB-блоков, которая поддерживает только хранение блоков BLOB-блоков.</span><span class="sxs-lookup"><span data-stu-id="52d3e-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="52d3e-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="52d3e-200">FileStorage.</span></span> <span data-ttu-id="52d3e-201">Учетная запись хранилища файлов, которая поддерживает только хранение файлов.</span><span class="sxs-lookup"><span data-stu-id="52d3e-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="52d3e-202">Значение по умолчанию — StorageV2.</span><span class="sxs-lookup"><span data-stu-id="52d3e-202">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="52d3e-203">-Location</span><span class="sxs-lookup"><span data-stu-id="52d3e-203">-Location</span></span>
<span data-ttu-id="52d3e-204">Определяет расположение создаемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="52d3e-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="52d3e-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="52d3e-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="52d3e-206">Минимальная версия TLS, разрешенная для запросов на хранение.</span><span class="sxs-lookup"><span data-stu-id="52d3e-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="52d3e-207">По умолчанию для этого свойства закончится значение TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="52d3e-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="52d3e-208">-Name</span><span class="sxs-lookup"><span data-stu-id="52d3e-208">-Name</span></span>
<span data-ttu-id="52d3e-209">Имя создаемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="52d3e-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="52d3e-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="52d3e-210">-NetworkRuleSet</span></span>
<span data-ttu-id="52d3e-211">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для определения значений сетевых свойств, таких как службы, разрешенные для обхода правил, и обработки запросов, которые не соответствуют ни одной из них.</span><span class="sxs-lookup"><span data-stu-id="52d3e-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="52d3e-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="52d3e-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="52d3e-213">Служба будет применять дополнительный уровень шифрования с управляемыми платформой ключами для неавторяых данных.</span><span class="sxs-lookup"><span data-stu-id="52d3e-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="52d3e-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d3e-214">-ResourceGroupName</span></span>
<span data-ttu-id="52d3e-215">Имя группы ресурсов, в которую нужно добавить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="52d3e-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="52d3e-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="52d3e-216">-SkuName</span></span>
<span data-ttu-id="52d3e-217">Указывает SKU учетной записи хранения, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52d3e-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="52d3e-218">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="52d3e-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52d3e-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="52d3e-219">Standard_LRS.</span></span> <span data-ttu-id="52d3e-220">Локальное избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="52d3e-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="52d3e-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="52d3e-221">Standard_ZRS.</span></span> <span data-ttu-id="52d3e-222">Избыточное хранилище зоны.</span><span class="sxs-lookup"><span data-stu-id="52d3e-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="52d3e-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="52d3e-223">Standard_GRS.</span></span> <span data-ttu-id="52d3e-224">Гео избыточный объем хранилища.</span><span class="sxs-lookup"><span data-stu-id="52d3e-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="52d3e-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="52d3e-225">Standard_RAGRS.</span></span> <span data-ttu-id="52d3e-226">Чтение геобытного хранилища в Access.</span><span class="sxs-lookup"><span data-stu-id="52d3e-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="52d3e-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="52d3e-227">Premium_LRS.</span></span> <span data-ttu-id="52d3e-228">"Премиум" — локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="52d3e-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="52d3e-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="52d3e-229">Premium_ZRS.</span></span> <span data-ttu-id="52d3e-230">Premium zone-redundant storage.</span><span class="sxs-lookup"><span data-stu-id="52d3e-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="52d3e-231">Standard_GZRS — гео-избыточное хранилище зоны— избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="52d3e-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="52d3e-232">Standard_RAGZRS — чтение доступа к гео-избыточной зоне, избыточный объем хранилища.</span><span class="sxs-lookup"><span data-stu-id="52d3e-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="52d3e-233">-Tag</span><span class="sxs-lookup"><span data-stu-id="52d3e-233">-Tag</span></span>
<span data-ttu-id="52d3e-234">Пары значений ключа в виде hash table set as tags (Теги на сервере).</span><span class="sxs-lookup"><span data-stu-id="52d3e-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="52d3e-235">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="52d3e-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="52d3e-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="52d3e-236">-UseSubDomain</span></span>
<span data-ttu-id="52d3e-237">Указывает, следует ли включить непрямую проверку CName.</span><span class="sxs-lookup"><span data-stu-id="52d3e-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="52d3e-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d3e-238">CommonParameters</span></span>
<span data-ttu-id="52d3e-239">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d3e-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d3e-240">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d3e-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d3e-241">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52d3e-241">INPUTS</span></span>

### <span data-ttu-id="52d3e-242">System.String</span><span class="sxs-lookup"><span data-stu-id="52d3e-242">System.String</span></span>

## <span data-ttu-id="52d3e-243">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52d3e-243">OUTPUTS</span></span>

### <span data-ttu-id="52d3e-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52d3e-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="52d3e-245">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="52d3e-245">NOTES</span></span>

## <span data-ttu-id="52d3e-246">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52d3e-246">RELATED LINKS</span></span>

[<span data-ttu-id="52d3e-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52d3e-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="52d3e-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52d3e-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="52d3e-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52d3e-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
