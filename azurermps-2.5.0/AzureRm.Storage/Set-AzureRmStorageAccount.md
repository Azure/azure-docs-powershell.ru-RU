---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: a6f16c4ef9012f7aaf5216e0cfb24edf65ce9f4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913716"
---
# <span data-ttu-id="fbf71-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbf71-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="fbf71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbf71-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf71-103">Изменение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fbf71-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbf71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbf71-104">SYNTAX</span></span>

### <span data-ttu-id="fbf71-105">StorageEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fbf71-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbf71-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="fbf71-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbf71-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbf71-107">DESCRIPTION</span></span>
<span data-ttu-id="fbf71-108">Командлет **Set-AzureRmStorageAccount** изменяет учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="fbf71-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="fbf71-109">Вы можете использовать этот командлет, чтобы изменить тип учетной записи, обновить домен клиента или настроить теги для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fbf71-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="fbf71-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbf71-110">EXAMPLES</span></span>

### <span data-ttu-id="fbf71-111">Пример 1: Настройка типа учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="fbf71-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="fbf71-112">Эта команда задает тип учетной записи хранения для Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="fbf71-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="fbf71-113">Пример 2: Настройка собственного домена для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="fbf71-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="fbf71-114">Эта команда задает настраиваемый домен для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fbf71-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="fbf71-115">Пример 3: Настройка значения уровня доступа</span><span class="sxs-lookup"><span data-stu-id="fbf71-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="fbf71-116">Команда задает для уровня доступа значение "круто".</span><span class="sxs-lookup"><span data-stu-id="fbf71-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="fbf71-117">Пример 4: Настройка собственного домена и тегов</span><span class="sxs-lookup"><span data-stu-id="fbf71-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="fbf71-118">Команда задает настраиваемый домен и теги для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fbf71-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="fbf71-119">Пример 5: Настройка шифрования KeySource на Keyvault</span><span class="sxs-lookup"><span data-stu-id="fbf71-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="fbf71-120">С помощью этой команды Настройте шифрование KeySource с новым созданным Keyvault.</span><span class="sxs-lookup"><span data-stu-id="fbf71-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="fbf71-121">Пример 6: Настройка шифрования KeySource на "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="fbf71-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="fbf71-122">Эта команда SET ENCRYPTION KeySource в "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="fbf71-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="fbf71-123">Пример 7: Настройка свойства NetworkRuleSet учетной записи хранения с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="fbf71-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="fbf71-124">Эта команда задает свойство NetworkRuleSet учетной записи хранения с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="fbf71-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="fbf71-125">Пример 8: получение свойства NetworkRuleSet из учетной записи хранения и задание другой учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="fbf71-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="fbf71-126">Первая команда получает свойство NetworkRuleSet из учетной записи хранения, а вторая команда задает другую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="fbf71-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="fbf71-127">Пример 9: обновление учетной записи хранения с помощью типа "хранилище" или "BlobStorage" на "StorageV2", "изменить учетную запись хранения"</span><span class="sxs-lookup"><span data-stu-id="fbf71-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="fbf71-128">Команда обновляет учетную запись хранения, которая имеет значение "хранилище" или "BlobStorage", в "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="fbf71-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

## <span data-ttu-id="fbf71-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbf71-129">PARAMETERS</span></span>

### <span data-ttu-id="fbf71-130">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="fbf71-130">-AccessTier</span></span>
<span data-ttu-id="fbf71-131">Указывает уровень доступа учетной записи хранения, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fbf71-131">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="fbf71-132">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="fbf71-132">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="fbf71-133">Изменение уровня доступа может привести к появлению дополнительных расходов.</span><span class="sxs-lookup"><span data-stu-id="fbf71-133">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="fbf71-134">Дополнительные сведения можно найти в разделе [хранилище BLOB-объектов Azure: уровни горячего и изящного хранилища](https://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="fbf71-134">For more information, see [Azure Blob Storage: Hot and cool storage tiers](https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="fbf71-135">Если учетная запись хранения имеет роль StorageV2 или BlobStorage, вы можете указать параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="fbf71-135">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="fbf71-136">Если для учетной записи хранения задано значение "хранилище", не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="fbf71-136">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="fbf71-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbf71-137">-AsJob</span></span>
<span data-ttu-id="fbf71-138">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fbf71-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbf71-139">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fbf71-139">-AssignIdentity</span></span>
<span data-ttu-id="fbf71-140">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="fbf71-140">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fbf71-141">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="fbf71-141">-CustomDomainName</span></span>
<span data-ttu-id="fbf71-142">Указывает имя настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="fbf71-142">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="fbf71-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf71-143">-DefaultProfile</span></span>
<span data-ttu-id="fbf71-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbf71-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf71-145">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="fbf71-145">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="fbf71-146">Указывает, разрешено ли учетной записи хранения только трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fbf71-146">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf71-147">-Force</span><span class="sxs-lookup"><span data-stu-id="fbf71-147">-Force</span></span>
<span data-ttu-id="fbf71-148">Принудительно заносит изменения в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="fbf71-148">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="fbf71-149">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fbf71-149">-KeyName</span></span>
<span data-ttu-id="fbf71-150">Если для включения шифрования с помощью ключа используется параметр-KeyvaultEncryption, укажите свойство KeyName с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="fbf71-150">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="fbf71-151">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="fbf71-151">-KeyvaultEncryption</span></span>
<span data-ttu-id="fbf71-152">Указывает, следует ли использовать Microsoft KeyVault для ключа шифрования при использовании шифрования службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="fbf71-152">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="fbf71-153">Если задано значение KeyName, KeyVersion и KeyVaultUri, KeySource будет установлено в Microsoft. Keyvault, установлен ли этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fbf71-153">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="fbf71-154">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="fbf71-154">-KeyVaultUri</span></span>
<span data-ttu-id="fbf71-155">При использовании шифрования с помощью ключа, указав параметр-KeyvaultEncryption, используйте этот параметр, чтобы указать универсальный код ресурса (URI) для ключевого хранилища.</span><span class="sxs-lookup"><span data-stu-id="fbf71-155">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="fbf71-156">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="fbf71-156">-KeyVersion</span></span>
<span data-ttu-id="fbf71-157">При использовании шифрования с помощью ключа, указав параметр-KeyvaultEncryption, используйте этот параметр, чтобы указать универсальный код ресурса (URI) для ключевой версии.</span><span class="sxs-lookup"><span data-stu-id="fbf71-157">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="fbf71-158">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fbf71-158">-Name</span></span>
<span data-ttu-id="fbf71-159">Указывает имя учетной записи хранения, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="fbf71-159">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="fbf71-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fbf71-160">-NetworkRuleSet</span></span>
<span data-ttu-id="fbf71-161">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, таких как службы, которые могут обойти правила и обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="fbf71-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="fbf71-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf71-162">-ResourceGroupName</span></span>
<span data-ttu-id="fbf71-163">Указывает имя группы ресурсов, в которой нужно изменить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="fbf71-163">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="fbf71-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fbf71-164">-SkuName</span></span>
<span data-ttu-id="fbf71-165">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fbf71-165">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="fbf71-166">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fbf71-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fbf71-167">Standard_LRS локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="fbf71-167">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="fbf71-168">Standard_ZRS — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="fbf71-168">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="fbf71-169">Standard_GRS геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="fbf71-169">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="fbf71-170">Standard_RAGRS — геоизбыточное хранилище, доступное для чтения.</span><span class="sxs-lookup"><span data-stu-id="fbf71-170">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="fbf71-171">Локальное хранилище с резервированием Premium_LRS Premium.</span><span class="sxs-lookup"><span data-stu-id="fbf71-171">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="fbf71-172">Вы не можете изменить Standard_ZRS и Premium_LRS типы для других типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="fbf71-172">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="fbf71-173">Нельзя изменить другие типы счетов на Standard_ZRS и Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="fbf71-173">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="fbf71-174">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="fbf71-174">-StorageEncryption</span></span>
<span data-ttu-id="fbf71-175">Указывает, следует ли настраивать шифрование учетной записи хранения для использования клавиш, управляемых корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="fbf71-175">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="fbf71-176">-Тег</span><span class="sxs-lookup"><span data-stu-id="fbf71-176">-Tag</span></span>
<span data-ttu-id="fbf71-177">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="fbf71-177">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="fbf71-178">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="fbf71-178">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fbf71-179">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="fbf71-179">-UpgradeToStorageV2</span></span>
<span data-ttu-id="fbf71-180">Обновите учетную запись хранения или BlobStorage в StorageV2.</span><span class="sxs-lookup"><span data-stu-id="fbf71-180">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="fbf71-181">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="fbf71-181">-UseSubDomain</span></span>
<span data-ttu-id="fbf71-182">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="fbf71-182">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="fbf71-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbf71-183">-Confirm</span></span>
<span data-ttu-id="fbf71-184">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbf71-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbf71-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbf71-185">-WhatIf</span></span>
<span data-ttu-id="fbf71-186">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbf71-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbf71-187">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbf71-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbf71-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf71-188">CommonParameters</span></span>
<span data-ttu-id="fbf71-189">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbf71-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf71-190">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbf71-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf71-191">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbf71-191">INPUTS</span></span>

### <span data-ttu-id="fbf71-192">System. String</span><span class="sxs-lookup"><span data-stu-id="fbf71-192">System.String</span></span>

### <span data-ttu-id="fbf71-193">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbf71-193">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fbf71-194">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fbf71-194">System.Boolean</span></span>

## <span data-ttu-id="fbf71-195">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbf71-195">OUTPUTS</span></span>

### <span data-ttu-id="fbf71-196">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbf71-196">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fbf71-197">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbf71-197">NOTES</span></span>

## <span data-ttu-id="fbf71-198">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbf71-198">RELATED LINKS</span></span>

[<span data-ttu-id="fbf71-199">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbf71-199">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="fbf71-200">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbf71-200">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="fbf71-201">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbf71-201">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)
