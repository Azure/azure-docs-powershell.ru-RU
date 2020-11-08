---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243806"
---
# <span data-ttu-id="9a3ce-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a3ce-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="9a3ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="9a3ce-103">Создание учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-103">Creates a Storage account.</span></span>

## <span data-ttu-id="9a3ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a3ce-104">SYNTAX</span></span>

### <span data-ttu-id="9a3ce-105">AzureActiveDirectoryDomainServicesForFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a3ce-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a3ce-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="9a3ce-106">ActiveDirectoryDomainServicesForFile</span></span>
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

## <span data-ttu-id="9a3ce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a3ce-107">DESCRIPTION</span></span>
<span data-ttu-id="9a3ce-108">Командлет **New-AzStorageAccount** создает учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="9a3ce-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a3ce-109">EXAMPLES</span></span>

### <span data-ttu-id="9a3ce-110">Пример 1: создание учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9a3ce-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="9a3ce-111">Эта команда создает учетную запись хранения для имени группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="9a3ce-112">Пример 2: создание учетной записи хранения BLOB-данных с BlobStorageным и горячим AccessTier</span><span class="sxs-lookup"><span data-stu-id="9a3ce-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="9a3ce-113">Эта команда создает учетную запись хранилища BLOB-объектов, которая имеет BlobStorage и горячий AccessTier</span><span class="sxs-lookup"><span data-stu-id="9a3ce-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="9a3ce-114">Пример 3: создание учетной записи хранения с помощью StorageV2, создание и назначение удостоверения для Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="9a3ce-115">Эта команда создает учетную запись хранения с StorageV2.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="9a3ce-116">Кроме того, она генерирует и назначает удостоверение, которое можно использовать для управления ключами учетной записи через Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="9a3ce-117">Пример 4: создание учетной записи хранения с помощью NetworkRuleSet из JSON</span><span class="sxs-lookup"><span data-stu-id="9a3ce-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="9a3ce-118">Эта команда создает учетную запись хранения, которая имеет свойство NetworkRuleSet из JSON.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="9a3ce-119">Пример 5: создание учетной записи хранения с включенным иерархическое пространством имен.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="9a3ce-120">Эта команда создает учетную запись хранения, для которой включено иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="9a3ce-121">Пример 6: создание учетной записи хранения для файлов Azure проверка подлинности в DS и включение больших файловых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="9a3ce-122">Эта команда создает учетную запись хранения для файлов Azure Authentication DS и обеспечивает большую общую доступ к файлам.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="9a3ce-123">Пример 7: создание учетной записи хранения с включенной проверкой подлинности доменной службы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="9a3ce-124">Эта команда создает учетную запись хранилища withenable файлов, подлинность которых доменная служба Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="9a3ce-125">Пример 8. Создание учетной записи хранения с помощью очереди и службы таблиц. Используйте ключ шифрования для учетной записи, а для этого требуется шифрование инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="9a3ce-126">Эта команда создает учетную запись хранения, в которой служба очереди и таблица использует ключ шифрования с областью действия для учетной записи, и для этого требуется шифрование инфраструктуры, поэтому в очереди и таблице используется один и тот же ключ шифрования с BLOB-объектов и службой файлов, и служба применяет дополнительный слой шифрования с управляемыми ключами платформы для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="9a3ce-127">Затем получите доступ к свойствам учетной записи хранения и просмотрите набор шифрования для службы очереди и таблицы, а также значение RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="9a3ce-128">Пример 9: создание учетной записи MinimumTlsVersion и AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="9a3ce-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="9a3ce-129">Команда создать учетную запись с помощью MinimumTlsVersion и AllowBlobPublicAccess и показать 2 свойства созданной учетной записи</span><span class="sxs-lookup"><span data-stu-id="9a3ce-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="9a3ce-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a3ce-130">PARAMETERS</span></span>

### <span data-ttu-id="9a3ce-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="9a3ce-131">-AccessTier</span></span>
<span data-ttu-id="9a3ce-132">Указывает уровень доступа учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="9a3ce-133">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="9a3ce-134">Если указать значение BlobStorage для параметра *вида* , необходимо указать значение параметра *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="9a3ce-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="9a3ce-135">Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="9a3ce-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="9a3ce-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="9a3ce-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="9a3ce-137">Задает идентификатор безопасности (SID) для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="9a3ce-138">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="9a3ce-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="9a3ce-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="9a3ce-140">Указывает GUID домена.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-140">Specifies the domain GUID.</span></span> <span data-ttu-id="9a3ce-141">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="9a3ce-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="9a3ce-143">Указывает основной домен, для которого авторизован DNS-сервер AD.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="9a3ce-144">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="9a3ce-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="9a3ce-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="9a3ce-146">Задает идентификатор безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="9a3ce-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="9a3ce-147">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="9a3ce-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="9a3ce-149">Указывает имя леса Active Directory, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="9a3ce-150">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="9a3ce-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="9a3ce-152">Задает доменное имя NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="9a3ce-153">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="9a3ce-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="9a3ce-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="9a3ce-155">Разрешить общий доступ ко всем BLOB-объектам или контейнерам в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="9a3ce-156">Для этого свойства интерпретация по умолчанию имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="9a3ce-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a3ce-157">-AsJob</span></span>
<span data-ttu-id="9a3ce-158">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9a3ce-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a3ce-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9a3ce-159">-AssignIdentity</span></span>
<span data-ttu-id="9a3ce-160">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9a3ce-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-161">-CustomDomainName</span></span>
<span data-ttu-id="9a3ce-162">Указывает имя настраиваемого домена учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="9a3ce-163">По умолчанию используется значение Storage.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="9a3ce-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a3ce-164">-DefaultProfile</span></span>
<span data-ttu-id="9a3ce-165">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a3ce-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="9a3ce-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="9a3ce-167">Включите проверку подлинности доменных служб Active Directory для учетной записи хранения в Azure Files.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="9a3ce-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="9a3ce-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="9a3ce-169">Включите проверку подлинности доменных служб Azure Active Directory для учетной записи хранения в Azure Files.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="9a3ce-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="9a3ce-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="9a3ce-171">Указывает, включено ли в учетной записи хранения иерархическое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="9a3ce-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="9a3ce-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="9a3ce-173">Указывает, разрешено ли учетной записи хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="9a3ce-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="9a3ce-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="9a3ce-175">Указывает, может ли учетная запись хранения поддерживать большие файловые ресурсы размером более 5 TiB.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="9a3ce-176">После включения учетной записи эту функцию нельзя отключить.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="9a3ce-177">В настоящее время поддерживается только для типов репликации LRS и ZRS, поэтому преобразование учетной записи в геоизбыточные учетные записи будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="9a3ce-178">Дополнительные сведения https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="9a3ce-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="9a3ce-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="9a3ce-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="9a3ce-180">Установка KeyType для шифрования в очереди.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="9a3ce-181">По умолчанию используется значение Service.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-181">The default value is Service.</span></span>
<span data-ttu-id="9a3ce-182">-Account: очередь будет зашифрована с использованием ключа шифрования с областью действия для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="9a3ce-183">-Service: очередь всегда будет шифроваться с помощью Service-Managed клавиш.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="9a3ce-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="9a3ce-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="9a3ce-185">Задайте для свойства KeyType для таблицы ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="9a3ce-186">По умолчанию используется значение Service.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-186">The default value is Service.</span></span>
- <span data-ttu-id="9a3ce-187">Учетная запись: таблица будет зашифрована с использованием ключа шифрования уровня учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="9a3ce-188">Служба: таблица всегда будет шифроваться с помощью Service-Managed клавиш.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="9a3ce-189">-Видах</span><span class="sxs-lookup"><span data-stu-id="9a3ce-189">-Kind</span></span>
<span data-ttu-id="9a3ce-190">Указывает вариант учетной записи хранения, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="9a3ce-191">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9a3ce-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a3ce-192">Склад.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-192">Storage.</span></span> <span data-ttu-id="9a3ce-193">Общая цель учетной записи хранения, которая поддерживает хранение больших двоичных объектов, таблиц, очередей, файлов и дисков.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="9a3ce-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-194">StorageV2.</span></span> <span data-ttu-id="9a3ce-195">Учетная запись хранения общего назначения версии 2 (GPv2), поддерживающая большие двоичные объекты, таблицы, очереди, файлы и диски, с дополнительными возможностями, такими как уровни данных.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="9a3ce-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-196">BlobStorage.</span></span> <span data-ttu-id="9a3ce-197">Учетная запись хранилища BLOB-объектов, поддерживающая только хранение больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="9a3ce-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-198">BlockBlobStorage.</span></span> <span data-ttu-id="9a3ce-199">Блокировка учетной записи хранения BLOB-объектов, которая поддерживает хранение блочных больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="9a3ce-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-200">FileStorage.</span></span> <span data-ttu-id="9a3ce-201">Учетная запись хранилища файлов, поддерживающая хранение только файлов.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="9a3ce-202">Значением по умолчанию является StorageV2.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-202">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="9a3ce-203">-Location</span><span class="sxs-lookup"><span data-stu-id="9a3ce-203">-Location</span></span>
<span data-ttu-id="9a3ce-204">Указывает расположение учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="9a3ce-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="9a3ce-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="9a3ce-206">Минимальная версия TLS, разрешаемая на запросы к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="9a3ce-207">Для этого свойства по умолчанию используется интерпретация TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="9a3ce-208">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a3ce-208">-Name</span></span>
<span data-ttu-id="9a3ce-209">Указывает имя учетной записи хранения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="9a3ce-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a3ce-210">-NetworkRuleSet</span></span>
<span data-ttu-id="9a3ce-211">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, таких как службы, которые могут обойти правила и обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="9a3ce-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="9a3ce-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="9a3ce-213">Служба применяет дополнительный слой шифрования с управляемыми ключами платформы для данных на остальных платформах.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="9a3ce-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-214">-ResourceGroupName</span></span>
<span data-ttu-id="9a3ce-215">Указывает имя группы ресурсов, в которую нужно добавить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="9a3ce-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9a3ce-216">-SkuName</span></span>
<span data-ttu-id="9a3ce-217">Указывает имя SKU учетной записи хранения, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="9a3ce-218">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9a3ce-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a3ce-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-219">Standard_LRS.</span></span> <span data-ttu-id="9a3ce-220">Локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="9a3ce-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-221">Standard_ZRS.</span></span> <span data-ttu-id="9a3ce-222">Зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="9a3ce-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-223">Standard_GRS.</span></span> <span data-ttu-id="9a3ce-224">Геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="9a3ce-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-225">Standard_RAGRS.</span></span> <span data-ttu-id="9a3ce-226">Доступное для чтения геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="9a3ce-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-227">Premium_LRS.</span></span> <span data-ttu-id="9a3ce-228">Локально — избыточное хранилище Premium.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="9a3ce-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-229">Premium_ZRS.</span></span> <span data-ttu-id="9a3ce-230">Расширенная зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="9a3ce-231">Standard_GZRS геоизбыточной зоны (избыточное хранилище).</span><span class="sxs-lookup"><span data-stu-id="9a3ce-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="9a3ce-232">Standard_RAGZRS-для чтения с геоизбыточной зоны (избыточное хранилище).</span><span class="sxs-lookup"><span data-stu-id="9a3ce-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="9a3ce-233">-Тег</span><span class="sxs-lookup"><span data-stu-id="9a3ce-233">-Tag</span></span>
<span data-ttu-id="9a3ce-234">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="9a3ce-235">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="9a3ce-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9a3ce-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="9a3ce-236">-UseSubDomain</span></span>
<span data-ttu-id="9a3ce-237">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="9a3ce-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a3ce-238">CommonParameters</span></span>
<span data-ttu-id="9a3ce-239">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a3ce-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a3ce-240">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a3ce-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a3ce-241">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a3ce-241">INPUTS</span></span>

### <span data-ttu-id="9a3ce-242">System. String</span><span class="sxs-lookup"><span data-stu-id="9a3ce-242">System.String</span></span>

## <span data-ttu-id="9a3ce-243">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a3ce-243">OUTPUTS</span></span>

### <span data-ttu-id="9a3ce-244">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a3ce-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9a3ce-245">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a3ce-245">NOTES</span></span>

## <span data-ttu-id="9a3ce-246">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a3ce-246">RELATED LINKS</span></span>

[<span data-ttu-id="9a3ce-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a3ce-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="9a3ce-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a3ce-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="9a3ce-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9a3ce-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
