---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912749"
---
# <span data-ttu-id="26012-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26012-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="26012-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26012-102">SYNOPSIS</span></span>
<span data-ttu-id="26012-103">Добавляет существующую учетную запись хранилища Azure в заданное хранилище ключей для ключей, управляемых службой хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="26012-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="26012-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26012-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26012-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26012-105">DESCRIPTION</span></span>
<span data-ttu-id="26012-106">Настройка существующей учетной записи хранилища Azure с хранилищем ключей для ключей учетной записи хранения для управления с помощью ключей.</span><span class="sxs-lookup"><span data-stu-id="26012-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="26012-107">Учетная запись хранения уже должна существовать.</span><span class="sxs-lookup"><span data-stu-id="26012-107">The Storage Account must already exist.</span></span> <span data-ttu-id="26012-108">Ключи хранилища никогда не открываются для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="26012-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="26012-109">Автоматическое повторное создание ключа и переключение активного ключа на основе периода повторного создания.</span><span class="sxs-lookup"><span data-stu-id="26012-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="26012-110">Общие сведения об этой функции см. в разделе " [управляемая учетная запись хранилища Azure Key" — PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) .</span><span class="sxs-lookup"><span data-stu-id="26012-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="26012-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26012-111">EXAMPLES</span></span>

### <span data-ttu-id="26012-112">Пример 1: Настройка учетной записи хранения Azure с помощью ключа Vault для управления ее ключами</span><span class="sxs-lookup"><span data-stu-id="26012-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="26012-113">Задает учетной записи хранения с основным хранилищем ключей для управления с помощью Key Vault.</span><span class="sxs-lookup"><span data-stu-id="26012-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="26012-114">Для активного ключа задано значение "key1".</span><span class="sxs-lookup"><span data-stu-id="26012-114">The active key set is 'key1'.</span></span> <span data-ttu-id="26012-115">Этот ключ будет использоваться для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="26012-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="26012-116">Ключевое приложение получит повторное создание ключа "key2" после периода повторного создания с момента выполнения этой команды и задает его в качестве активного ключа.</span><span class="sxs-lookup"><span data-stu-id="26012-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="26012-117">Этот процесс автоматического повторного создания продолжится между "key1" и "key2" с пропуском в 90 дней.</span><span class="sxs-lookup"><span data-stu-id="26012-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="26012-118">Пример 2: Настройка классической учетной записи хранилища Azure с помощью ключа Vault для управления ее ключами</span><span class="sxs-lookup"><span data-stu-id="26012-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="26012-119">Задает классический учетной записи хранилища с основным хранилищем ключей для управления с помощью Key Vault.</span><span class="sxs-lookup"><span data-stu-id="26012-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="26012-120">Активным является параметр "основной".</span><span class="sxs-lookup"><span data-stu-id="26012-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="26012-121">Этот ключ будет использоваться для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="26012-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="26012-122">Ключевое приложение получит повторное создание ключа "дополнительный" после периода повторного создания с момента этой команды и установит его в качестве активного ключа.</span><span class="sxs-lookup"><span data-stu-id="26012-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="26012-123">Этот процесс автоматического повторного создания продолжится между "основным" и "дополнительным" с пропуском в 90 дней.</span><span class="sxs-lookup"><span data-stu-id="26012-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="26012-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26012-124">PARAMETERS</span></span>

### <span data-ttu-id="26012-125">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="26012-125">-AccountName</span></span>
<span data-ttu-id="26012-126">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="26012-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="26012-127">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="26012-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="26012-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="26012-128">-AccountResourceId</span></span>
<span data-ttu-id="26012-129">Идентификатор ресурса Azure учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="26012-129">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="26012-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="26012-130">-ActiveKeyName</span></span>
<span data-ttu-id="26012-131">Имя ключа учетной записи хранения, которое необходимо использовать для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="26012-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="26012-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26012-132">-DefaultProfile</span></span>
<span data-ttu-id="26012-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="26012-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26012-134">-Отключение</span><span class="sxs-lookup"><span data-stu-id="26012-134">-Disable</span></span>
<span data-ttu-id="26012-135">Отключение использования ключа управляемой учетной записи хранения для создания маркеров SAS.</span><span class="sxs-lookup"><span data-stu-id="26012-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="26012-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="26012-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="26012-137">Автоматическое повторное создание ключа.</span><span class="sxs-lookup"><span data-stu-id="26012-137">Auto regenerate key.</span></span> <span data-ttu-id="26012-138">Если установлено значение true, неактивный ключ для управляемой учетной записи хранения будет автоматически восстановлен и станет новым активным ключом после периода повторного создания.</span><span class="sxs-lookup"><span data-stu-id="26012-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="26012-139">Если задано значение false, ключи управляемой учетной записи хранения не воссоздаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="26012-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="26012-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="26012-140">-RegenerationPeriod</span></span>
<span data-ttu-id="26012-141">Период повторного создания.</span><span class="sxs-lookup"><span data-stu-id="26012-141">Regeneration period.</span></span> <span data-ttu-id="26012-142">Если включено автоматическое повторное создание ключа, это значение определяет интервал времени, после которого функция автоматического повторного создания keygets управляемой учетной записи хранилища становится новым активным ключом.</span><span class="sxs-lookup"><span data-stu-id="26012-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="26012-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="26012-143">-Tag</span></span>
<span data-ttu-id="26012-144">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="26012-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="26012-145">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="26012-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="26012-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="26012-146">-VaultName</span></span>
<span data-ttu-id="26012-147">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="26012-147">Vault name.</span></span>
<span data-ttu-id="26012-148">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="26012-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="26012-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26012-149">-Confirm</span></span>
<span data-ttu-id="26012-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26012-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26012-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26012-151">-WhatIf</span></span>
<span data-ttu-id="26012-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26012-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26012-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26012-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26012-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26012-154">CommonParameters</span></span>
<span data-ttu-id="26012-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26012-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26012-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26012-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26012-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26012-157">INPUTS</span></span>

### <span data-ttu-id="26012-158">System. String</span><span class="sxs-lookup"><span data-stu-id="26012-158">System.String</span></span>

### <span data-ttu-id="26012-159">System. Nullable "1 [[System. TimeSpan, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26012-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="26012-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="26012-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="26012-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26012-161">OUTPUTS</span></span>

### <span data-ttu-id="26012-162">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26012-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="26012-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="26012-163">NOTES</span></span>

## <span data-ttu-id="26012-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26012-164">RELATED LINKS</span></span>

[<span data-ttu-id="26012-165">AZ. KeyVault</span><span class="sxs-lookup"><span data-stu-id="26012-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
