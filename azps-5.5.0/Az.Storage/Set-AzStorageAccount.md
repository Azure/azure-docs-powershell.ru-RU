---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 4a4898645e3f296f861aa9f19a60ea182c112bff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217241"
---
# <span data-ttu-id="bafee-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bafee-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="bafee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bafee-102">SYNOPSIS</span></span>
<span data-ttu-id="bafee-103">Изменяет учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="bafee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bafee-104">SYNTAX</span></span>

### <span data-ttu-id="bafee-105">StorageEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bafee-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bafee-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="bafee-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bafee-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="bafee-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bafee-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bafee-108">DESCRIPTION</span></span>
<span data-ttu-id="bafee-109">**Cmdlet Set-AzStorageAccount** изменяет учетную запись хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bafee-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="bafee-110">С помощью этого командлета можно изменить тип учетной записи, обновить домен клиента или настроить теги для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="bafee-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bafee-111">EXAMPLES</span></span>

### <span data-ttu-id="bafee-112">Пример 1. Настройка типа учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bafee-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="bafee-113">Эта команда задает для учетной записи хранения Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="bafee-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="bafee-114">Пример 2. Настройка пользовательского домена для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bafee-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="bafee-115">Эта команда задает настраиваемый домен для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="bafee-116">Пример 3. Настройка уровня доступа</span><span class="sxs-lookup"><span data-stu-id="bafee-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="bafee-117">Команда задает для уровня Access действительное значение.</span><span class="sxs-lookup"><span data-stu-id="bafee-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="bafee-118">Пример 4. Настройка пользовательского домена и тегов</span><span class="sxs-lookup"><span data-stu-id="bafee-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="bafee-119">Она задает настраиваемый домен и теги для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="bafee-120">Пример 5. Установите Keyvault в качестве ключевого ключа шифрования</span><span class="sxs-lookup"><span data-stu-id="bafee-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="bafee-121">Этот набор команд наборов ключей шифрования с новым значением Keyvault.</span><span class="sxs-lookup"><span data-stu-id="bafee-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="bafee-122">Пример 6. Задай для ключей шифрования значение Microsoft.Storage.</span><span class="sxs-lookup"><span data-stu-id="bafee-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="bafee-123">Этот командный пункт "Ключ шифрования" задает для службы Microsoft.Storage значение "Microsoft.Storage".</span><span class="sxs-lookup"><span data-stu-id="bafee-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="bafee-124">Пример 7. Настройка свойства NetworkRuleSet учетной записи хранения с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="bafee-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="bafee-125">Эта команда задает свойство NetworkRuleSet учетной записи хранения с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="bafee-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="bafee-126">Пример 8. Получить свойство NetworkRuleSet из учетной записи хранения и настроить его на другую учетную запись хранения</span><span class="sxs-lookup"><span data-stu-id="bafee-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="bafee-127">Эта первая команда получает свойство NetworkRuleSet из учетной записи хранения, а вторая задает для него другую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="bafee-128">Пример 9. Обновление учетной записи хранения с помощью kind "Storage" или "BlobStorage" до "StorageV2" вида "Учетная запись хранения"</span><span class="sxs-lookup"><span data-stu-id="bafee-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="bafee-129">Команда обновит учетную запись хранения с kind "Storage" или "BlobStorage" до "StorageV2" вида "Хранилище".</span><span class="sxs-lookup"><span data-stu-id="bafee-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="bafee-130">Пример 10. Обновление учетной записи хранения путем обеспечения проверки подлинности Azure Files AAD DS.</span><span class="sxs-lookup"><span data-stu-id="bafee-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="bafee-131">Команда обновляет учетную запись хранения, в результате этого включается проверка подлинности AAD DS для файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="bafee-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="bafee-132">Пример 11. Обновление учетной записи хранения путем вирования проверки подлинности доменной службы Files Active Directory и показа параметра проверки подлинности на основе идентификаторов файлов</span><span class="sxs-lookup"><span data-stu-id="bafee-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
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

<span data-ttu-id="bafee-133">Команда обновляет учетную запись хранения, в результате чего включается проверка подлинности доменной службы Azure Files Active Directory, а затем показан параметр проверки подлинности на основе удостоверений файлов.</span><span class="sxs-lookup"><span data-stu-id="bafee-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="bafee-134">Пример 12: Set MinimumTlsVersion и AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="bafee-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="bafee-135">Команда задает MinimumTlsVersion и AllowBlobPublicAccess, а затем показывает 2 свойства учетной записи.</span><span class="sxs-lookup"><span data-stu-id="bafee-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

### <span data-ttu-id="bafee-136">Пример 13. Обновление учетной записи хранения с помощью параметра RoutingPreference</span><span class="sxs-lookup"><span data-stu-id="bafee-136">Example 13: Update a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -PublishMicrosoftEndpoint $false -PublishInternetEndpoint $true -RoutingChoice InternetRouting

PS C:\>$account.RoutingPreference

RoutingChoice   PublishMicrosoftEndpoints PublishInternetEndpoints
-------------   ------------------------- ------------------------
InternetRouting                     False                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : 
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="bafee-137">Эта команда обновляет учетную запись хранения с параметром RoutingPreference: PublishMicrosoftEndpoint как false, PublishInternetEndpoint как true и RoutingChoice как MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="bafee-137">This command updates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint as false, PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="bafee-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bafee-138">PARAMETERS</span></span>

### <span data-ttu-id="bafee-139">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="bafee-139">-AccessTier</span></span>
<span data-ttu-id="bafee-140">Определяет уровень доступа к учетной записи хранения, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafee-140">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="bafee-141">Допустимыми значениями для этого параметра являются hot and Cool.</span><span class="sxs-lookup"><span data-stu-id="bafee-141">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="bafee-142">Изменение уровня доступа может привести к дополнительным затратам.</span><span class="sxs-lookup"><span data-stu-id="bafee-142">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="bafee-143">Дополнительные сведения см. в хранилище [BLOB-хранилищ Azure: уровни хранилища — "Hot" и "Классный".](http://go.microsoft.com/fwlink/?LinkId=786482)</span><span class="sxs-lookup"><span data-stu-id="bafee-143">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="bafee-144">Если у учетной записи хранения есть Kind as StorageV2 или BlobStorage, вы можете указать параметр *AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="bafee-144">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="bafee-145">Если у учетной записи хранения есть kind as Storage, не укажите параметр *AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="bafee-145">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="bafee-146">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="bafee-146">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="bafee-147">Определяет идентификатор безопасности для хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="bafee-147">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="bafee-148">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="bafee-148">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bafee-149">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="bafee-149">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="bafee-150">Определяет GUID домена.</span><span class="sxs-lookup"><span data-stu-id="bafee-150">Specifies the domain GUID.</span></span> <span data-ttu-id="bafee-151">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="bafee-151">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bafee-152">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="bafee-152">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="bafee-153">Определяет основной домен, для который является полномочного DNS-сервером AD.</span><span class="sxs-lookup"><span data-stu-id="bafee-153">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="bafee-154">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="bafee-154">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bafee-155">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="bafee-155">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="bafee-156">Идентификатор безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="bafee-156">Specifies the security identifier (SID).</span></span> <span data-ttu-id="bafee-157">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="bafee-157">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bafee-158">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="bafee-158">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="bafee-159">Указывает лес Active Directory, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="bafee-159">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="bafee-160">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="bafee-160">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bafee-161">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="bafee-161">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="bafee-162">Указывает доменное имя NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="bafee-162">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="bafee-163">Этот параметр должен быть задан, если для параметра -EnableActiveDirectoryDomainServicesForFile установлено true.</span><span class="sxs-lookup"><span data-stu-id="bafee-163">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bafee-164">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="bafee-164">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="bafee-165">Разрешение или депустив общедоступный доступ ко всем BLOB-данным или контейнерам в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-165">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="bafee-166">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bafee-166">-AsJob</span></span>
<span data-ttu-id="bafee-167">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bafee-167">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bafee-168">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="bafee-168">-AssignIdentity</span></span>
<span data-ttu-id="bafee-169">Создание и назначение удостоверения учетной записи хранения для этой учетной записи хранения для использования с основными службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="bafee-169">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="bafee-170">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="bafee-170">-CustomDomainName</span></span>
<span data-ttu-id="bafee-171">Указывает имя пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="bafee-171">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="bafee-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafee-172">-DefaultProfile</span></span>
<span data-ttu-id="bafee-173">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bafee-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bafee-174">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="bafee-174">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="bafee-175">В этой службе можно включить проверку подлинности доменной службы Azure Files Active Directory для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="bafee-176">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="bafee-176">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="bafee-177">В этой службе можно включить проверку подлинности доменной службы Azure Files Active Directory для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-177">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="bafee-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="bafee-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="bafee-179">Указывает, включает ли учетная запись хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bafee-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="bafee-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="bafee-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="bafee-181">Указывает, поддерживает ли учетная запись хранения большие папки емкостью более 5 ТБ.</span><span class="sxs-lookup"><span data-stu-id="bafee-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="bafee-182">После включения учетной записи эту функцию невозможно отключить.</span><span class="sxs-lookup"><span data-stu-id="bafee-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="bafee-183">В настоящее время поддерживается только для типов репликации LRS и ZRS, поэтому преобразование учетных записей в геоизбыточные учетные записи невозможно.</span><span class="sxs-lookup"><span data-stu-id="bafee-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="bafee-184">Подробнее в https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="bafee-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="bafee-185">-Force</span><span class="sxs-lookup"><span data-stu-id="bafee-185">-Force</span></span>
<span data-ttu-id="bafee-186">В этом сценарии изменения будут записаны в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-186">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="bafee-187">-KeyName</span><span class="sxs-lookup"><span data-stu-id="bafee-187">-KeyName</span></span>
<span data-ttu-id="bafee-188">Если для шифрования с хранилищем ключей используется шифрование -KeyvaultEncryption, укажите свойство "Имя ключа" с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="bafee-188">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="bafee-189">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="bafee-189">-KeyvaultEncryption</span></span>
<span data-ttu-id="bafee-190">Указывает, следует ли использовать ключ KeyVault Microsoft keyVault для ключей шифрования при использовании шифрования службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="bafee-190">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="bafee-191">Если параметр KeyName, KeyVersion и KeyVaultUri задан, параметр KeySource будет иметь значение Microsoft.Keyvault независимо от того, задан ли этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bafee-191">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="bafee-192">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="bafee-192">-KeyVaultUri</span></span>
<span data-ttu-id="bafee-193">При использовании шифрования key Vault путем указания параметра -KeyvaultEncryption используйте этот параметр, чтобы указать URI для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="bafee-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="bafee-194">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="bafee-194">-KeyVersion</span></span>
<span data-ttu-id="bafee-195">При использовании шифрования key Vault путем указания параметра -KeyvaultEncryption используйте этот параметр, чтобы указать URI для версии ключа.</span><span class="sxs-lookup"><span data-stu-id="bafee-195">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="bafee-196">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="bafee-196">-MinimumTlsVersion</span></span>
<span data-ttu-id="bafee-197">Минимальная версия TLS, разрешенная для запросов на хранение.</span><span class="sxs-lookup"><span data-stu-id="bafee-197">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="bafee-198">-Name</span><span class="sxs-lookup"><span data-stu-id="bafee-198">-Name</span></span>
<span data-ttu-id="bafee-199">Указывает имя изменяемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-199">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="bafee-200">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bafee-200">-NetworkRuleSet</span></span>
<span data-ttu-id="bafee-201">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для определения значений сетевых свойств, таких как службы, разрешенные для обхода правил, и обработки запросов, которые не соответствуют ни одной из них.</span><span class="sxs-lookup"><span data-stu-id="bafee-201">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="bafee-202">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="bafee-202">-PublishInternetEndpoint</span></span>
<span data-ttu-id="bafee-203">Указывает на возможность публикации конечных точек хранилища маршрутов в Интернете</span><span class="sxs-lookup"><span data-stu-id="bafee-203">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="bafee-204">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="bafee-204">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="bafee-205">Указывает, должны ли публиковаться конечные точки хранилища маршрутов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="bafee-205">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="bafee-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bafee-206">-ResourceGroupName</span></span>
<span data-ttu-id="bafee-207">Указывает имя группы ресурсов, в которой нужно изменить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-207">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="bafee-208">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="bafee-208">-RoutingChoice</span></span>
<span data-ttu-id="bafee-209">Выбор маршрутии определяет тип сетевой маршрутии, opted пользователем.</span><span class="sxs-lookup"><span data-stu-id="bafee-209">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="bafee-210">Возможные значения: "MicrosoftRouting", "InternetRouting"</span><span class="sxs-lookup"><span data-stu-id="bafee-210">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="bafee-211">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bafee-211">-SkuName</span></span>
<span data-ttu-id="bafee-212">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-212">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="bafee-213">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="bafee-213">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bafee-214">Standard_LRS — локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="bafee-214">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="bafee-215">Standard_ZRS — избыточное хранилище зоны.</span><span class="sxs-lookup"><span data-stu-id="bafee-215">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="bafee-216">Standard_GRS — гео-избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="bafee-216">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="bafee-217">Standard_RAGRS — чтение геообытного хранилища для доступа.</span><span class="sxs-lookup"><span data-stu-id="bafee-217">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="bafee-218">Premium_LRS — локально избыточное хранилище Premium.</span><span class="sxs-lookup"><span data-stu-id="bafee-218">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="bafee-219">Standard_GZRS — гео-избыточное хранилище зоны— избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="bafee-219">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="bafee-220">Standard_RAGZRS — чтение доступа к гео-избыточной зоне, избыточный объем хранилища.</span><span class="sxs-lookup"><span data-stu-id="bafee-220">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="bafee-221">Типы учетных Standard_ZRS и Premium_LRS нельзя изменить на другие типы учетных записей.</span><span class="sxs-lookup"><span data-stu-id="bafee-221">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="bafee-222">Другие типы учетных записей нельзя Standard_ZRS или Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="bafee-222">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="bafee-223">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="bafee-223">-StorageEncryption</span></span>
<span data-ttu-id="bafee-224">Указывает, нужно ли использовать ключи, управляемые Майкрософт, для шифрования учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bafee-224">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="bafee-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="bafee-225">-Tag</span></span>
<span data-ttu-id="bafee-226">Пары значений ключа в виде hash table set as tags (Теги на сервере).</span><span class="sxs-lookup"><span data-stu-id="bafee-226">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="bafee-227">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="bafee-227">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bafee-228">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="bafee-228">-UpgradeToStorageV2</span></span>
<span data-ttu-id="bafee-229">Обновив учетную запись хранения Kind с Storage или BlobStorage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="bafee-229">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="bafee-230">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="bafee-230">-UseSubDomain</span></span>
<span data-ttu-id="bafee-231">Указывает, следует ли включить непрямую проверку CName.</span><span class="sxs-lookup"><span data-stu-id="bafee-231">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="bafee-232">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bafee-232">-Confirm</span></span>
<span data-ttu-id="bafee-233">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafee-233">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bafee-234">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bafee-234">-WhatIf</span></span>
<span data-ttu-id="bafee-235">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafee-235">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bafee-236">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bafee-236">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bafee-237">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafee-237">CommonParameters</span></span>
<span data-ttu-id="bafee-238">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bafee-238">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafee-239">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bafee-239">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafee-240">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bafee-240">INPUTS</span></span>

### <span data-ttu-id="bafee-241">System.String</span><span class="sxs-lookup"><span data-stu-id="bafee-241">System.String</span></span>

### <span data-ttu-id="bafee-242">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bafee-242">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bafee-243">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bafee-243">OUTPUTS</span></span>

### <span data-ttu-id="bafee-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bafee-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="bafee-245">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bafee-245">NOTES</span></span>

## <span data-ttu-id="bafee-246">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bafee-246">RELATED LINKS</span></span>

[<span data-ttu-id="bafee-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bafee-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="bafee-248">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bafee-248">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="bafee-249">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bafee-249">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
