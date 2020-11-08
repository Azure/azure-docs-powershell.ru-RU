---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245779"
---
# <span data-ttu-id="dd3b0-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3b0-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="dd3b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="dd3b0-103">Изменение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="dd3b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd3b0-104">SYNTAX</span></span>

### <span data-ttu-id="dd3b0-105">StorageEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd3b0-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd3b0-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="dd3b0-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd3b0-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="dd3b0-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd3b0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd3b0-108">DESCRIPTION</span></span>
<span data-ttu-id="dd3b0-109">Командлет **Set-AzStorageAccount** изменяет учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="dd3b0-110">Вы можете использовать этот командлет, чтобы изменить тип учетной записи, обновить домен клиента или настроить теги для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="dd3b0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd3b0-111">EXAMPLES</span></span>

### <span data-ttu-id="dd3b0-112">Пример 1: Настройка типа учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="dd3b0-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="dd3b0-113">Эта команда задает тип учетной записи хранения для Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="dd3b0-114">Пример 2: Настройка собственного домена для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="dd3b0-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="dd3b0-115">Эта команда задает настраиваемый домен для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="dd3b0-116">Пример 3: Настройка значения уровня доступа</span><span class="sxs-lookup"><span data-stu-id="dd3b0-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="dd3b0-117">Команда задает для уровня доступа значение "круто".</span><span class="sxs-lookup"><span data-stu-id="dd3b0-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="dd3b0-118">Пример 4: Настройка собственного домена и тегов</span><span class="sxs-lookup"><span data-stu-id="dd3b0-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="dd3b0-119">Команда задает настраиваемый домен и теги для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="dd3b0-120">Пример 5: Настройка шифрования KeySource на Keyvault</span><span class="sxs-lookup"><span data-stu-id="dd3b0-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="dd3b0-121">С помощью этой команды Настройте шифрование KeySource с новым созданным Keyvault.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="dd3b0-122">Пример 6: Настройка шифрования KeySource на "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="dd3b0-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="dd3b0-123">Эта команда SET ENCRYPTION KeySource в "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="dd3b0-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="dd3b0-124">Пример 7: Настройка свойства NetworkRuleSet учетной записи хранения с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="dd3b0-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="dd3b0-125">Эта команда задает свойство NetworkRuleSet учетной записи хранения с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="dd3b0-126">Пример 8: получение свойства NetworkRuleSet из учетной записи хранения и задание другой учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="dd3b0-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="dd3b0-127">Первая команда получает свойство NetworkRuleSet из учетной записи хранения, а вторая команда задает другую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="dd3b0-128">Пример 9: обновление учетной записи хранения с помощью типа "хранилище" или "BlobStorage" на "StorageV2", "изменить учетную запись хранения"</span><span class="sxs-lookup"><span data-stu-id="dd3b0-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="dd3b0-129">Команда обновляет учетную запись хранения, которая имеет значение "хранилище" или "BlobStorage", в "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="dd3b0-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="dd3b0-130">Пример 10. Обновите учетную запись хранения, включив файлы Azure Authentication DS для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="dd3b0-131">Эта команда обновляет учетную запись хранения, включив файлы Azure для проверки подлинности DS доменных служб AAD.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="dd3b0-132">Пример 11: обновление учетной записи хранения путем включения проверки подлинности доменных служб Active Directory и последующего отображения параметра проверки подлинности на основе удостоверения файла</span><span class="sxs-lookup"><span data-stu-id="dd3b0-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="dd3b0-133">Эта команда обновляет учетную запись хранения, активируя проверку подлинности доменных служб Active Directory для файлов Azure, а затем показывает параметры проверки подлинности на основе удостоверения файла.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="dd3b0-134">Пример 12: Настройка MinimumTlsVersion и AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="dd3b0-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="dd3b0-135">Команда задает MinimumTlsVersion и AllowBlobPublicAccess, а затем показывает 2 свойства учетной записи.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="dd3b0-136">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd3b0-136">PARAMETERS</span></span>

### <span data-ttu-id="dd3b0-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="dd3b0-137">-AccessTier</span></span>
<span data-ttu-id="dd3b0-138">Указывает уровень доступа учетной записи хранения, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="dd3b0-139">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="dd3b0-140">Изменение уровня доступа может привести к появлению дополнительных расходов.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="dd3b0-141">Дополнительные сведения можно найти в разделе [хранилище BLOB-объектов Azure: уровни горячего и изящного хранилища](http://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="dd3b0-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="dd3b0-142">Если учетная запись хранения имеет роль StorageV2 или BlobStorage, вы можете указать параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="dd3b0-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="dd3b0-143">Если для учетной записи хранения задано значение "хранилище", не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="dd3b0-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="dd3b0-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="dd3b0-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="dd3b0-145">Задает идентификатор безопасности (SID) для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="dd3b0-146">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="dd3b0-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="dd3b0-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="dd3b0-148">Указывает GUID домена.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-148">Specifies the domain GUID.</span></span> <span data-ttu-id="dd3b0-149">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="dd3b0-150">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="dd3b0-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="dd3b0-151">Указывает основной домен, для которого авторизован DNS-сервер AD.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="dd3b0-152">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="dd3b0-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="dd3b0-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="dd3b0-154">Задает идентификатор безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="dd3b0-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="dd3b0-155">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="dd3b0-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="dd3b0-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="dd3b0-157">Указывает имя леса Active Directory, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="dd3b0-158">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="dd3b0-159">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="dd3b0-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="dd3b0-160">Задает доменное имя NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="dd3b0-161">Этот параметр должен быть установлен, если для параметра-EnableActiveDirectoryDomainServicesForFile задано значение true.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="dd3b0-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="dd3b0-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="dd3b0-163">Разрешение или запрет общего доступа ко всем BLOB-объектам или контейнерам в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="dd3b0-164">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd3b0-164">-AsJob</span></span>
<span data-ttu-id="dd3b0-165">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dd3b0-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd3b0-166">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="dd3b0-166">-AssignIdentity</span></span>
<span data-ttu-id="dd3b0-167">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="dd3b0-168">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="dd3b0-168">-CustomDomainName</span></span>
<span data-ttu-id="dd3b0-169">Указывает имя настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-169">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="dd3b0-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd3b0-170">-DefaultProfile</span></span>
<span data-ttu-id="dd3b0-171">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd3b0-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="dd3b0-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="dd3b0-173">Включите проверку подлинности доменных служб Active Directory для учетной записи хранения в Azure Files.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="dd3b0-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="dd3b0-175">Включите проверку подлинности доменных служб Active Directory для учетной записи хранения в Azure Files.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="dd3b0-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="dd3b0-177">Указывает, разрешено ли учетной записи хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="dd3b0-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="dd3b0-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="dd3b0-179">Указывает, может ли учетная запись хранения поддерживать большие файловые ресурсы размером более 5 TiB.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="dd3b0-180">После включения учетной записи эту функцию нельзя отключить.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="dd3b0-181">В настоящее время поддерживается только для типов репликации LRS и ZRS, поэтому преобразование учетной записи в геоизбыточные учетные записи будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="dd3b0-182">Дополнительные сведения https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="dd3b0-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="dd3b0-183">-Force</span><span class="sxs-lookup"><span data-stu-id="dd3b0-183">-Force</span></span>
<span data-ttu-id="dd3b0-184">Принудительно заносит изменения в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="dd3b0-185">-KeyName</span><span class="sxs-lookup"><span data-stu-id="dd3b0-185">-KeyName</span></span>
<span data-ttu-id="dd3b0-186">Если для включения шифрования с помощью ключа используется параметр-KeyvaultEncryption, укажите свойство KeyName с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="dd3b0-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="dd3b0-188">Указывает, следует ли использовать Microsoft KeyVault для ключа шифрования при использовании шифрования службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="dd3b0-189">Если задано значение KeyName, KeyVersion и KeyVaultUri, KeySource будет установлено в Microsoft. Keyvault, установлен ли этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="dd3b0-190">-KeyVaultUri</span></span>
<span data-ttu-id="dd3b0-191">При использовании шифрования с помощью ключа, указав параметр-KeyvaultEncryption, используйте этот параметр, чтобы указать универсальный код ресурса (URI) для ключевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-192">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="dd3b0-192">-KeyVersion</span></span>
<span data-ttu-id="dd3b0-193">При использовании шифрования с помощью ключа, указав параметр-KeyvaultEncryption, используйте этот параметр, чтобы указать универсальный код ресурса (URI) для ключевой версии.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-194">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="dd3b0-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="dd3b0-195">Минимальная версия TLS, разрешаемая на запросы к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-195">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="dd3b0-196">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd3b0-196">-Name</span></span>
<span data-ttu-id="dd3b0-197">Указывает имя учетной записи хранения, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-197">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="dd3b0-198">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd3b0-198">-NetworkRuleSet</span></span>
<span data-ttu-id="dd3b0-199">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, таких как службы, которые могут обойти правила и обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="dd3b0-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd3b0-200">-ResourceGroupName</span></span>
<span data-ttu-id="dd3b0-201">Указывает имя группы ресурсов, в которой нужно изменить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="dd3b0-202">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dd3b0-202">-SkuName</span></span>
<span data-ttu-id="dd3b0-203">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="dd3b0-204">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="dd3b0-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd3b0-205">Standard_LRS локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="dd3b0-206">Standard_ZRS — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="dd3b0-207">Standard_GRS геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="dd3b0-208">Standard_RAGRS — геоизбыточное хранилище, доступное для чтения.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="dd3b0-209">Локальное хранилище с резервированием Premium_LRS Premium.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="dd3b0-210">Standard_GZRS геоизбыточной зоны (избыточное хранилище).</span><span class="sxs-lookup"><span data-stu-id="dd3b0-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="dd3b0-211">Standard_RAGZRS-для чтения с геоизбыточной зоны (избыточное хранилище).</span><span class="sxs-lookup"><span data-stu-id="dd3b0-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="dd3b0-212">Вы не можете изменить Standard_ZRS и Premium_LRS типы для других типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="dd3b0-213">Нельзя изменить другие типы счетов на Standard_ZRS и Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="dd3b0-214">-StorageEncryption</span></span>
<span data-ttu-id="dd3b0-215">Указывает, следует ли настраивать шифрование учетной записи хранения для использования клавиш, управляемых корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-216">-Тег</span><span class="sxs-lookup"><span data-stu-id="dd3b0-216">-Tag</span></span>
<span data-ttu-id="dd3b0-217">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="dd3b0-218">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="dd3b0-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="dd3b0-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="dd3b0-220">Обновите учетную запись хранения или BlobStorage в StorageV2.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="dd3b0-221">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="dd3b0-221">-UseSubDomain</span></span>
<span data-ttu-id="dd3b0-222">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-222">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="dd3b0-223">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd3b0-223">-Confirm</span></span>
<span data-ttu-id="dd3b0-224">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd3b0-225">-WhatIf</span></span>
<span data-ttu-id="dd3b0-226">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd3b0-227">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-227">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3b0-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3b0-228">CommonParameters</span></span>
<span data-ttu-id="dd3b0-229">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd3b0-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd3b0-230">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd3b0-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3b0-231">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd3b0-231">INPUTS</span></span>

### <span data-ttu-id="dd3b0-232">System. String</span><span class="sxs-lookup"><span data-stu-id="dd3b0-232">System.String</span></span>

### <span data-ttu-id="dd3b0-233">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dd3b0-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dd3b0-234">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd3b0-234">OUTPUTS</span></span>

### <span data-ttu-id="dd3b0-235">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3b0-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="dd3b0-236">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd3b0-236">NOTES</span></span>

## <span data-ttu-id="dd3b0-237">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd3b0-237">RELATED LINKS</span></span>

[<span data-ttu-id="dd3b0-238">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3b0-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="dd3b0-239">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3b0-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="dd3b0-240">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dd3b0-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
