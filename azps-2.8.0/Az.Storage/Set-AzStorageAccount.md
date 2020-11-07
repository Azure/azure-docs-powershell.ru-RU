---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 69c71cd0401b8509943ef7e5ad7316db99f03670
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907470"
---
# <span data-ttu-id="6a66f-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a66f-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="6a66f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a66f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a66f-103">Изменение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6a66f-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="6a66f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a66f-104">SYNTAX</span></span>

### <span data-ttu-id="6a66f-105">StorageEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6a66f-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a66f-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="6a66f-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a66f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a66f-107">DESCRIPTION</span></span>
<span data-ttu-id="6a66f-108">Командлет **Set-AzStorageAccount** изменяет учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="6a66f-108">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="6a66f-109">Вы можете использовать этот командлет, чтобы изменить тип учетной записи, обновить домен клиента или настроить теги для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6a66f-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="6a66f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a66f-110">EXAMPLES</span></span>

### <span data-ttu-id="6a66f-111">Пример 1: Настройка типа учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6a66f-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="6a66f-112">Эта команда задает тип учетной записи хранения для Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="6a66f-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="6a66f-113">Пример 2: Настройка собственного домена для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6a66f-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="6a66f-114">Эта команда задает настраиваемый домен для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6a66f-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="6a66f-115">Пример 3: Настройка значения уровня доступа</span><span class="sxs-lookup"><span data-stu-id="6a66f-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="6a66f-116">Команда задает для уровня доступа значение "круто".</span><span class="sxs-lookup"><span data-stu-id="6a66f-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="6a66f-117">Пример 4: Настройка собственного домена и тегов</span><span class="sxs-lookup"><span data-stu-id="6a66f-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="6a66f-118">Команда задает настраиваемый домен и теги для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6a66f-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="6a66f-119">Пример 5: Настройка шифрования KeySource на Keyvault</span><span class="sxs-lookup"><span data-stu-id="6a66f-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="6a66f-120">С помощью этой команды Настройте шифрование KeySource с новым созданным Keyvault.</span><span class="sxs-lookup"><span data-stu-id="6a66f-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="6a66f-121">Пример 6: Настройка шифрования KeySource на "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="6a66f-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="6a66f-122">Эта команда SET ENCRYPTION KeySource в "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="6a66f-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="6a66f-123">Пример 7: Настройка свойства NetworkRuleSet учетной записи хранения с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="6a66f-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="6a66f-124">Эта команда задает свойство NetworkRuleSet учетной записи хранения с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="6a66f-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="6a66f-125">Пример 8: получение свойства NetworkRuleSet из учетной записи хранения и задание другой учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6a66f-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="6a66f-126">Первая команда получает свойство NetworkRuleSet из учетной записи хранения, а вторая команда задает другую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="6a66f-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="6a66f-127">Пример 9: обновление учетной записи хранения с помощью типа "хранилище" или "BlobStorage" на "StorageV2", "изменить учетную запись хранения"</span><span class="sxs-lookup"><span data-stu-id="6a66f-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="6a66f-128">Команда обновляет учетную запись хранения, которая имеет значение "хранилище" или "BlobStorage", в "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="6a66f-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="6a66f-129">Пример 10. Обновите учетную запись хранения, включив файлы Azure Authentication DS для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="6a66f-129">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="6a66f-130">Эта команда обновляет учетную запись хранения, включив файлы Azure для проверки подлинности DS доменных служб AAD.</span><span class="sxs-lookup"><span data-stu-id="6a66f-130">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="6a66f-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a66f-131">PARAMETERS</span></span>

### <span data-ttu-id="6a66f-132">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="6a66f-132">-AccessTier</span></span>
<span data-ttu-id="6a66f-133">Указывает уровень доступа учетной записи хранения, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6a66f-133">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="6a66f-134">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="6a66f-134">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="6a66f-135">Изменение уровня доступа может привести к появлению дополнительных расходов.</span><span class="sxs-lookup"><span data-stu-id="6a66f-135">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="6a66f-136">Дополнительные сведения можно найти в разделе [хранилище BLOB-объектов Azure: уровни горячего и изящного хранилища](https://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="6a66f-136">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="6a66f-137">Если учетная запись хранения имеет роль StorageV2 или BlobStorage, вы можете указать параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="6a66f-137">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="6a66f-138">Если для учетной записи хранения задано значение "хранилище", не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="6a66f-138">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="6a66f-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a66f-139">-AsJob</span></span>
<span data-ttu-id="6a66f-140">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6a66f-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a66f-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6a66f-141">-AssignIdentity</span></span>
<span data-ttu-id="6a66f-142">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="6a66f-142">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="6a66f-143">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="6a66f-143">-CustomDomainName</span></span>
<span data-ttu-id="6a66f-144">Указывает имя настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="6a66f-144">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="6a66f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a66f-145">-DefaultProfile</span></span>
<span data-ttu-id="6a66f-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a66f-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a66f-147">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="6a66f-147">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="6a66f-148">Включите проверку подлинности доменных служб Azure Active Directory для учетной записи хранения в Azure Files.</span><span class="sxs-lookup"><span data-stu-id="6a66f-148">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="6a66f-149">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="6a66f-149">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="6a66f-150">Указывает, разрешено ли учетной записи хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6a66f-150">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="6a66f-151">-Force</span><span class="sxs-lookup"><span data-stu-id="6a66f-151">-Force</span></span>
<span data-ttu-id="6a66f-152">Принудительно заносит изменения в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="6a66f-152">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="6a66f-153">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6a66f-153">-KeyName</span></span>
<span data-ttu-id="6a66f-154">Если для включения шифрования с помощью ключа используется параметр-KeyvaultEncryption, укажите свойство KeyName с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="6a66f-154">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="6a66f-155">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="6a66f-155">-KeyvaultEncryption</span></span>
<span data-ttu-id="6a66f-156">Указывает, следует ли использовать Microsoft KeyVault для ключа шифрования при использовании шифрования службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="6a66f-156">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="6a66f-157">Если задано значение KeyName, KeyVersion и KeyVaultUri, KeySource будет установлено в Microsoft. Keyvault, установлен ли этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6a66f-157">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="6a66f-158">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="6a66f-158">-KeyVaultUri</span></span>
<span data-ttu-id="6a66f-159">При использовании шифрования с помощью ключа, указав параметр-KeyvaultEncryption, используйте этот параметр, чтобы указать универсальный код ресурса (URI) для ключевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="6a66f-159">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="6a66f-160">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="6a66f-160">-KeyVersion</span></span>
<span data-ttu-id="6a66f-161">При использовании шифрования с помощью ключа, указав параметр-KeyvaultEncryption, используйте этот параметр, чтобы указать универсальный код ресурса (URI) для ключевой версии.</span><span class="sxs-lookup"><span data-stu-id="6a66f-161">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="6a66f-162">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6a66f-162">-Name</span></span>
<span data-ttu-id="6a66f-163">Указывает имя учетной записи хранения, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="6a66f-163">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="6a66f-164">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a66f-164">-NetworkRuleSet</span></span>
<span data-ttu-id="6a66f-165">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, таких как службы, которые могут обойти правила и обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="6a66f-165">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="6a66f-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a66f-166">-ResourceGroupName</span></span>
<span data-ttu-id="6a66f-167">Указывает имя группы ресурсов, в которой нужно изменить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="6a66f-167">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="6a66f-168">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6a66f-168">-SkuName</span></span>
<span data-ttu-id="6a66f-169">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6a66f-169">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="6a66f-170">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6a66f-170">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a66f-171">Standard_LRS локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="6a66f-171">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="6a66f-172">Standard_ZRS — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="6a66f-172">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="6a66f-173">Standard_GRS геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="6a66f-173">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="6a66f-174">Standard_RAGRS — геоизбыточное хранилище, доступное для чтения.</span><span class="sxs-lookup"><span data-stu-id="6a66f-174">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="6a66f-175">Локальное хранилище с резервированием Premium_LRS Premium.</span><span class="sxs-lookup"><span data-stu-id="6a66f-175">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="6a66f-176">Вы не можете изменить Standard_ZRS и Premium_LRS типы для других типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="6a66f-176">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="6a66f-177">Нельзя изменить другие типы счетов на Standard_ZRS и Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="6a66f-177">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a66f-178">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="6a66f-178">-StorageEncryption</span></span>
<span data-ttu-id="6a66f-179">Указывает, следует ли настраивать шифрование учетной записи хранения для использования клавиш, управляемых корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6a66f-179">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="6a66f-180">-Тег</span><span class="sxs-lookup"><span data-stu-id="6a66f-180">-Tag</span></span>
<span data-ttu-id="6a66f-181">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="6a66f-181">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="6a66f-182">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="6a66f-182">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6a66f-183">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="6a66f-183">-UpgradeToStorageV2</span></span>
<span data-ttu-id="6a66f-184">Обновите учетную запись хранения или BlobStorage в StorageV2.</span><span class="sxs-lookup"><span data-stu-id="6a66f-184">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="6a66f-185">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="6a66f-185">-UseSubDomain</span></span>
<span data-ttu-id="6a66f-186">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="6a66f-186">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="6a66f-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a66f-187">-Confirm</span></span>
<span data-ttu-id="6a66f-188">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6a66f-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a66f-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a66f-189">-WhatIf</span></span>
<span data-ttu-id="6a66f-190">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6a66f-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a66f-191">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6a66f-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a66f-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a66f-192">CommonParameters</span></span>
<span data-ttu-id="6a66f-193">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a66f-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a66f-194">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a66f-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a66f-195">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a66f-195">INPUTS</span></span>

### <span data-ttu-id="6a66f-196">System. String</span><span class="sxs-lookup"><span data-stu-id="6a66f-196">System.String</span></span>

### <span data-ttu-id="6a66f-197">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6a66f-197">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6a66f-198">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a66f-198">OUTPUTS</span></span>

### <span data-ttu-id="6a66f-199">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a66f-199">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6a66f-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a66f-200">NOTES</span></span>

## <span data-ttu-id="6a66f-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a66f-201">RELATED LINKS</span></span>

[<span data-ttu-id="6a66f-202">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a66f-202">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="6a66f-203">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a66f-203">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="6a66f-204">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a66f-204">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
