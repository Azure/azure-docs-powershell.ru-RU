---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518385"
---
# <span data-ttu-id="f7e46-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7e46-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="f7e46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7e46-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e46-103">Добавляет существующую учетную запись хранилища Azure в указанное хранилище ключей для управления ключами службой key Vault.</span><span class="sxs-lookup"><span data-stu-id="f7e46-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="f7e46-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7e46-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7e46-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7e46-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e46-106">Настраивает существующую учетную запись хранилища Azure с ключным хранилищем для управления ключами учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7e46-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="f7e46-107">Учетная запись хранения должна уже существовать.</span><span class="sxs-lookup"><span data-stu-id="f7e46-107">The Storage Account must already exist.</span></span> <span data-ttu-id="f7e46-108">Ключи хранения никогда не 2010 2013 не аются для вызываемого устройства.</span><span class="sxs-lookup"><span data-stu-id="f7e46-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="f7e46-109">Key Vault auto regenerates and switches the active key based on the period.</span><span class="sxs-lookup"><span data-stu-id="f7e46-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="f7e46-110">Обзор [этой функции см. в powerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) для учетной записи управляемого хранилища key Vault Azure.</span><span class="sxs-lookup"><span data-stu-id="f7e46-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="f7e46-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7e46-111">EXAMPLES</span></span>

### <span data-ttu-id="f7e46-112">Пример 1. Настройка учетной записи хранилища Azure с хранилищем ключа для управления ключами</span><span class="sxs-lookup"><span data-stu-id="f7e46-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="f7e46-113">Задает учетную запись хранения с ключным хранилищем, чтобы управлять ключами из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f7e46-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="f7e46-114">Активный набор клавиш имеет значение "ключ1".</span><span class="sxs-lookup"><span data-stu-id="f7e46-114">The active key set is 'key1'.</span></span> <span data-ttu-id="f7e46-115">Этот ключ будет использоваться для создания токенов sas.</span><span class="sxs-lookup"><span data-stu-id="f7e46-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="f7e46-116">Key Vault will regenerate 'key2' after the period from the time of this command and set it as the active key.</span><span class="sxs-lookup"><span data-stu-id="f7e46-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="f7e46-117">Этот процесс автоматической обработки будет продолжаться между ключами 1 и 2 с пропажами в 90 дней.</span><span class="sxs-lookup"><span data-stu-id="f7e46-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="f7e46-118">Пример 2. Настройка классической учетной записи хранения Azure с хранилищем ключей для управления ключами</span><span class="sxs-lookup"><span data-stu-id="f7e46-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="f7e46-119">Задает классическую учетную запись хранения с ключным хранилищем, чтобы управлять ключами из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f7e46-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="f7e46-120">Для активного ключа замерен первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="f7e46-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="f7e46-121">Этот ключ будет использоваться для создания токенов sas.</span><span class="sxs-lookup"><span data-stu-id="f7e46-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="f7e46-122">Key Vault will regenerate 'Secondary' key after the period from the time of this command and set it as the active key.</span><span class="sxs-lookup"><span data-stu-id="f7e46-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="f7e46-123">Этот процесс автоматической обработки будет продолжаться между первичным и дополнительным с пропажами в 90 дней.</span><span class="sxs-lookup"><span data-stu-id="f7e46-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="f7e46-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7e46-124">PARAMETERS</span></span>

### <span data-ttu-id="f7e46-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f7e46-125">-AccountName</span></span>
<span data-ttu-id="f7e46-126">Имя учетной записи управляемого хранилища в key Vault.</span><span class="sxs-lookup"><span data-stu-id="f7e46-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="f7e46-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span><span class="sxs-lookup"><span data-stu-id="f7e46-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7e46-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f7e46-128">-AccountResourceId</span></span>
<span data-ttu-id="f7e46-129">ИД ресурса Azure для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f7e46-129">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7e46-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="f7e46-130">-ActiveKeyName</span></span>
<span data-ttu-id="f7e46-131">Имя ключа учетной записи хранения, который должен использоваться для создания маркеров sas.</span><span class="sxs-lookup"><span data-stu-id="f7e46-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="f7e46-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e46-132">-DefaultProfile</span></span>
<span data-ttu-id="f7e46-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7e46-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7e46-134">-Disable</span><span class="sxs-lookup"><span data-stu-id="f7e46-134">-Disable</span></span>
<span data-ttu-id="f7e46-135">Отключает использование ключа учетной записи управляемого хранилища для генерации маркеров sas.</span><span class="sxs-lookup"><span data-stu-id="f7e46-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="f7e46-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="f7e46-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="f7e46-137">Клавиша автоматического повторного сгенерации.</span><span class="sxs-lookup"><span data-stu-id="f7e46-137">Auto regenerate key.</span></span> <span data-ttu-id="f7e46-138">Если это так, то неактивный ключ учетной записи хранения автоматически сгенерируется и становится новым активным ключом после расчетного периода.</span><span class="sxs-lookup"><span data-stu-id="f7e46-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="f7e46-139">Если этот ложь, ключи управляемой учетной записи хранения не сгенерированы автоматически.</span><span class="sxs-lookup"><span data-stu-id="f7e46-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="f7e46-140">-СкайпПериод</span><span class="sxs-lookup"><span data-stu-id="f7e46-140">-RegenerationPeriod</span></span>
<span data-ttu-id="f7e46-141">Период засеки.</span><span class="sxs-lookup"><span data-stu-id="f7e46-141">Regeneration period.</span></span> <span data-ttu-id="f7e46-142">Если включено автоматическое сгенерированное ключ, это значение определяет период времени, после которого неактивные ключи будут сгенерированы автоматически и становятся активным ключом.</span><span class="sxs-lookup"><span data-stu-id="f7e46-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7e46-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7e46-143">-Tag</span></span>
<span data-ttu-id="f7e46-144">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="f7e46-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f7e46-145">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f7e46-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f7e46-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f7e46-146">-VaultName</span></span>
<span data-ttu-id="f7e46-147">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="f7e46-147">Vault name.</span></span>
<span data-ttu-id="f7e46-148">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="f7e46-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f7e46-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7e46-149">-Confirm</span></span>
<span data-ttu-id="f7e46-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7e46-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e46-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e46-151">-WhatIf</span></span>
<span data-ttu-id="f7e46-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7e46-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7e46-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f7e46-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e46-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e46-154">CommonParameters</span></span>
<span data-ttu-id="f7e46-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7e46-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e46-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7e46-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e46-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7e46-157">INPUTS</span></span>

### <span data-ttu-id="f7e46-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f7e46-158">System.String</span></span>

### <span data-ttu-id="f7e46-159">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f7e46-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f7e46-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f7e46-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f7e46-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7e46-161">OUTPUTS</span></span>

### <span data-ttu-id="f7e46-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7e46-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="f7e46-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7e46-163">NOTES</span></span>

## <span data-ttu-id="f7e46-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7e46-164">RELATED LINKS</span></span>

[<span data-ttu-id="f7e46-165">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7e46-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
