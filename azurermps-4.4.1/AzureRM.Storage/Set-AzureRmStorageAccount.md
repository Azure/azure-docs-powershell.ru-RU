---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 5ca65c09746f6bb9a050c14fe10987702465b484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565099"
---
# <span data-ttu-id="d9be1-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9be1-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="d9be1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9be1-102">SYNOPSIS</span></span>
<span data-ttu-id="d9be1-103">Изменение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d9be1-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9be1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9be1-104">SYNTAX</span></span>

### <span data-ttu-id="d9be1-105">StorageEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9be1-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9be1-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="d9be1-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9be1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9be1-107">DESCRIPTION</span></span>
<span data-ttu-id="d9be1-108">Командлет **Set-AzureRmStorageAccount** изменяет учетную запись хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="d9be1-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="d9be1-109">Вы можете использовать этот командлет, чтобы изменить тип учетной записи, обновить домен клиента или настроить теги для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d9be1-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="d9be1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9be1-110">EXAMPLES</span></span>

### <span data-ttu-id="d9be1-111">Пример 1: Настройка типа учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d9be1-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="d9be1-112">Эта команда задает тип учетной записи хранения для Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="d9be1-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="d9be1-113">Пример 2: Настройка собственного домена для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d9be1-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="d9be1-114">Эта команда задает настраиваемый домен для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d9be1-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="d9be1-115">Пример 3: Включение шифрования для больших двоичных объектов и файловых служб</span><span class="sxs-lookup"><span data-stu-id="d9be1-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="d9be1-116">Эта команда включает шифрование службы хранилища для BLOB-объектов и файлов для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d9be1-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="d9be1-117">Пример 4: Настройка значения уровня доступа</span><span class="sxs-lookup"><span data-stu-id="d9be1-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="d9be1-118">Команда задает для уровня доступа значение "круто".</span><span class="sxs-lookup"><span data-stu-id="d9be1-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="d9be1-119">Пример 4: Настройка собственного домена и тегов</span><span class="sxs-lookup"><span data-stu-id="d9be1-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="d9be1-120">Команда задает для уровня доступа значение "круто".</span><span class="sxs-lookup"><span data-stu-id="d9be1-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="d9be1-121">Пример 5: Включение шифрования в службах BLOB с помощью Keyvault</span><span class="sxs-lookup"><span data-stu-id="d9be1-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="d9be1-122">Эта команда включает шифрование службы хранилища для BLOB с новым созданным Keyvault.</span><span class="sxs-lookup"><span data-stu-id="d9be1-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="d9be1-123">Пример 6: отключение шифрования в службах файлов с KeySource, установленным на "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="d9be1-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="d9be1-124">Эта команда отключает шифрование в файловых службах с помощью KeySource, установленного на Microsoft. Storage.</span><span class="sxs-lookup"><span data-stu-id="d9be1-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="d9be1-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9be1-125">PARAMETERS</span></span>

### <span data-ttu-id="d9be1-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="d9be1-126">-AccessTier</span></span>
<span data-ttu-id="d9be1-127">Указывает уровень доступа учетной записи хранения, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d9be1-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="d9be1-128">Допустимые значения этого параметра: горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="d9be1-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="d9be1-129">Изменение уровня доступа может привести к появлению дополнительных расходов.</span><span class="sxs-lookup"><span data-stu-id="d9be1-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="d9be1-130">Дополнительные сведения можно найти в хранилище больших двоичных объектов Azure: уровнях горячего и высококлассического хранилища https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="d9be1-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="d9be1-131">Если в качестве типа учетной записи хранения задано хранилище, не указывайте этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d9be1-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9be1-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d9be1-132">-AssignIdentity</span></span>
<span data-ttu-id="d9be1-133">Создание и назначение нового удостоверения учетной записи хранения для этой учетной записи хранения для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d9be1-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d9be1-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d9be1-134">-CustomDomainName</span></span>
<span data-ttu-id="d9be1-135">Указывает имя настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="d9be1-135">Specifies the name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9be1-136">-DisableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="d9be1-136">-DisableEncryptionService</span></span>
<span data-ttu-id="d9be1-137">Указывает, отключает ли этот командлет шифрование службы хранилища для службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="d9be1-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="d9be1-138">Поддерживаются двоичные файлы и службы Azure.</span><span class="sxs-lookup"><span data-stu-id="d9be1-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9be1-139">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="d9be1-139">-EnableEncryptionService</span></span>
<span data-ttu-id="d9be1-140">Указывает, включает ли этот командлет шифрование службы хранилища для службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="d9be1-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="d9be1-141">Поддерживаются двоичные файлы и службы Azure.</span><span class="sxs-lookup"><span data-stu-id="d9be1-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9be1-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="d9be1-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="d9be1-143">Указывает, следует ли учетной записи хранения включать трафик HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d9be1-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="d9be1-144">-Force</span><span class="sxs-lookup"><span data-stu-id="d9be1-144">-Force</span></span>
<span data-ttu-id="d9be1-145">Изменение уровня доступа может привести к появлению дополнительных расходов.</span><span class="sxs-lookup"><span data-stu-id="d9be1-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="d9be1-146">Дополнительные сведения можно найти в хранилище больших двоичных объектов Azure: уровнях горячего и высококлассического хранилища https://go.microsoft.com/fwlink/?LinkId=786482 ( https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="d9be1-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="d9be1-147">Если в качестве типа учетной записи хранения задано хранилище, не указывайте этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d9be1-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="d9be1-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d9be1-148">-InformationAction</span></span>
<span data-ttu-id="d9be1-149">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="d9be1-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d9be1-150">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d9be1-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9be1-151">Продолжал</span><span class="sxs-lookup"><span data-stu-id="d9be1-151">Continue</span></span>
- <span data-ttu-id="d9be1-152">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="d9be1-152">Ignore</span></span>
- <span data-ttu-id="d9be1-153">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="d9be1-153">Inquire</span></span>
- <span data-ttu-id="d9be1-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d9be1-154">SilentlyContinue</span></span>
- <span data-ttu-id="d9be1-155">Остановить</span><span class="sxs-lookup"><span data-stu-id="d9be1-155">Stop</span></span>
- <span data-ttu-id="d9be1-156">Рвать</span><span class="sxs-lookup"><span data-stu-id="d9be1-156">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9be1-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d9be1-157">-InformationVariable</span></span>
<span data-ttu-id="d9be1-158">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="d9be1-158">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9be1-159">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d9be1-159">-KeyName</span></span>
<span data-ttu-id="d9be1-160">Шифрование учетной записи хранения keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="d9be1-160">Storage Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="d9be1-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="d9be1-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="d9be1-162">Следует ли настроить шифрование учетной записи хранения KeySource в Microsoft. Keyvault или нет.</span><span class="sxs-lookup"><span data-stu-id="d9be1-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span> <span data-ttu-id="d9be1-163">Если указать параметр KeyName, KeyVersion и KeyvaultUri, для шифрования учетной записи хранения keySource также будет задано значение Microsoft. Keyvault weather.</span><span class="sxs-lookup"><span data-stu-id="d9be1-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
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

### <span data-ttu-id="d9be1-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="d9be1-164">-KeyVaultUri</span></span>
<span data-ttu-id="d9be1-165">Шифрование учетной записи хранения keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="d9be1-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="d9be1-166">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="d9be1-166">-KeyVersion</span></span>
<span data-ttu-id="d9be1-167">Шифрование учетной записи хранения keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="d9be1-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="d9be1-168">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9be1-168">-Name</span></span>
<span data-ttu-id="d9be1-169">Указывает имя учетной записи хранения, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="d9be1-169">Specifies the name of the Storage account to Modify.</span></span>

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

### <span data-ttu-id="d9be1-170">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d9be1-170">-NetworkRuleSet</span></span>
<span data-ttu-id="d9be1-171">NetworkRuleSet учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d9be1-171">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="d9be1-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9be1-172">-ResourceGroupName</span></span>
<span data-ttu-id="d9be1-173">Указывает имя группы ресурсов, в которой нужно изменить учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="d9be1-173">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="d9be1-174">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d9be1-174">-SkuName</span></span>
<span data-ttu-id="d9be1-175">Указывает имя SKU учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d9be1-175">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="d9be1-176">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d9be1-176">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d9be1-177">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="d9be1-177">Standard_LRS.</span></span>
<span data-ttu-id="d9be1-178">Локально избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="d9be1-178">Locally-redundant storage.</span></span> 
- <span data-ttu-id="d9be1-179">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="d9be1-179">Standard_ZRS.</span></span>
<span data-ttu-id="d9be1-180">Зона — избыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="d9be1-180">Zone-redundant storage.</span></span>
- <span data-ttu-id="d9be1-181">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="d9be1-181">Standard_GRS.</span></span>
<span data-ttu-id="d9be1-182">Геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="d9be1-182">Geo-redundant storage.</span></span> 
- <span data-ttu-id="d9be1-183">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="d9be1-183">Standard_RAGRS.</span></span>
<span data-ttu-id="d9be1-184">Доступное для чтения геоизбыточное хранилище.</span><span class="sxs-lookup"><span data-stu-id="d9be1-184">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="d9be1-185">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="d9be1-185">Premium_LRS.</span></span>
<span data-ttu-id="d9be1-186">Локально — избыточное хранилище Premium.</span><span class="sxs-lookup"><span data-stu-id="d9be1-186">Premium locally-redundant storage.</span></span>

<span data-ttu-id="d9be1-187">Вы не можете изменить Standard_ZRS и Premium_LRS типы для других типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d9be1-187">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="d9be1-188">Нельзя изменить другие типы счетов на Standard_ZRS и Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="d9be1-188">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9be1-189">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="d9be1-189">-StorageEncryption</span></span>
<span data-ttu-id="d9be1-190">Следует ли настроить шифрование учетной записи хранения KeySource в Microsoft. Storage или нет.</span><span class="sxs-lookup"><span data-stu-id="d9be1-190">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

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

### <span data-ttu-id="d9be1-191">-Тег</span><span class="sxs-lookup"><span data-stu-id="d9be1-191">-Tag</span></span>
<span data-ttu-id="d9be1-192">Если вы укажете значение BlobStorage для параметра *вида* в командлете New-AzureRmStorageAccount, необходимо указать значение параметра *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="d9be1-192">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="d9be1-193">Если для этого параметра *типа* задано значение хранилища, не указывайте параметр *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="d9be1-193">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9be1-194">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="d9be1-194">-UseSubDomain</span></span>
<span data-ttu-id="d9be1-195">Указывает, нужно ли включить косвенную проверку CName.</span><span class="sxs-lookup"><span data-stu-id="d9be1-195">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9be1-196">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9be1-196">-Confirm</span></span>
<span data-ttu-id="d9be1-197">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9be1-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9be1-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9be1-198">-WhatIf</span></span>
<span data-ttu-id="d9be1-199">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d9be1-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9be1-200">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9be1-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9be1-201">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9be1-201">-DefaultProfile</span></span>
<span data-ttu-id="d9be1-202">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9be1-202">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9be1-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9be1-203">CommonParameters</span></span>
<span data-ttu-id="d9be1-204">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9be1-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9be1-205">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9be1-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9be1-206">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9be1-206">INPUTS</span></span>

## <span data-ttu-id="d9be1-207">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9be1-207">OUTPUTS</span></span>

## <span data-ttu-id="d9be1-208">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9be1-208">NOTES</span></span>

## <span data-ttu-id="d9be1-209">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9be1-209">RELATED LINKS</span></span>

[<span data-ttu-id="d9be1-210">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9be1-210">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="d9be1-211">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9be1-211">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="d9be1-212">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9be1-212">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)


