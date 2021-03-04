---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ab126ee6bfc6a19f4a3a9997a75a01277437e42d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952515"
---
# <span data-ttu-id="4c8bb-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c8bb-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4c8bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c8bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4c8bb-103">Удаляет учетную запись хранения Azure с управляемым хранилищем Key Vault и все связанные определения SAS.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="4c8bb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4c8bb-104">SYNTAX</span></span>

### <span data-ttu-id="4c8bb-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="4c8bb-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c8bb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4c8bb-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c8bb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c8bb-107">DESCRIPTION</span></span>
<span data-ttu-id="4c8bb-108">Развязает учетную запись хранения Azure из key Vault.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="4c8bb-109">При этом учетная запись хранения Azure не удаляется, но из хранилища ключей Azure не удаляются ключи учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="4c8bb-110">Удаляются все связанные определения SAS хранилища, связанные с хранилищем.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="4c8bb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4c8bb-111">EXAMPLES</span></span>

### <span data-ttu-id="4c8bb-112">Пример 1. Удаление ключевого хранилища, управляемой учетной записью хранилища Azure, и всех связанных определений SAS.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="4c8bb-113">Разсогласовка учетной записи хранения Azure с mystorageaccount из key Vault myvault и остановка управления ключом хранилища.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="4c8bb-114">Учетная запись mystorageaccount не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="4c8bb-115">Все определения SAS хранилища, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="4c8bb-116">Пример 2. Удаление учетной записи хранилища Azure с управляемым хранилищем Key Vault и всех связанных определений SAS без подтверждения пользователем.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="4c8bb-117">Разсогласовка учетной записи хранения Azure с mystorageaccount из key Vault myvault и остановка управления ключом хранилища.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="4c8bb-118">Учетная запись mystorageaccount не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="4c8bb-119">Все определения SAS хранилища, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="4c8bb-120">Пример 3. Окончательное удаление (очистка) учетной записи хранилища Azure с управляемым хранилищем Azure и всех связанных определений SAS из хранилища с поддержкой soft-delete.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="4c8bb-121">Предполагается, что для этого хранилища включено неявное удаление.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="4c8bb-122">Проверьте, так ли это, проверив свойства хранилища или атрибут RecoveryLevel для сущности в сейфе.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="4c8bb-123">Первый cmdlet disassociates Azure Storage Account 'mystorageaccount' из key Vault 'myvault' и останавливает key Vault from managing its keys.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="4c8bb-124">Учетная запись mystorageaccount не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="4c8bb-125">Все определения SAS хранилища, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="4c8bb-126">Второй cmdlet проверяет, что учетная запись хранения удалена, но в состоянии восстановления.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="4c8bb-127">Для достижения этого состояния может потребоваться некоторое время. Перед попыткой разрешить около 30 м.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="4c8bb-128">Третий из них удаляет учетную запись хранения без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="4c8bb-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c8bb-129">PARAMETERS</span></span>

### <span data-ttu-id="4c8bb-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4c8bb-130">-AccountName</span></span>
<span data-ttu-id="4c8bb-131">Имя учетной записи, управляемой хранилищем Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="4c8bb-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c8bb-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c8bb-133">-DefaultProfile</span></span>
<span data-ttu-id="4c8bb-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4c8bb-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c8bb-135">-Force</span><span class="sxs-lookup"><span data-stu-id="4c8bb-135">-Force</span></span>
<span data-ttu-id="4c8bb-136">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4c8bb-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c8bb-137">-InputObject</span></span>
<span data-ttu-id="4c8bb-138">Объект ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-138">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c8bb-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4c8bb-139">-InRemovedState</span></span>
<span data-ttu-id="4c8bb-140">Окончательное удаление ранее удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="4c8bb-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c8bb-141">-PassThru</span></span>
<span data-ttu-id="4c8bb-142">По умолчанию cmdlet не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4c8bb-143">Если этот переключатель задан, возвращается удаленная учетная запись управляемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="4c8bb-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4c8bb-144">-VaultName</span></span>
<span data-ttu-id="4c8bb-145">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-145">Vault name.</span></span>
<span data-ttu-id="4c8bb-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c8bb-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c8bb-147">-Confirm</span></span>
<span data-ttu-id="4c8bb-148">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c8bb-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c8bb-149">-WhatIf</span></span>
<span data-ttu-id="4c8bb-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c8bb-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c8bb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c8bb-152">CommonParameters</span></span>
<span data-ttu-id="4c8bb-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c8bb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c8bb-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c8bb-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c8bb-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c8bb-155">INPUTS</span></span>

### <span data-ttu-id="4c8bb-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4c8bb-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="4c8bb-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c8bb-157">OUTPUTS</span></span>

### <span data-ttu-id="4c8bb-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c8bb-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="4c8bb-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4c8bb-159">NOTES</span></span>

## <span data-ttu-id="4c8bb-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c8bb-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

