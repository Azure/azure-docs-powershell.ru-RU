---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250208"
---
# <span data-ttu-id="eea6e-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eea6e-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="eea6e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eea6e-102">SYNOPSIS</span></span>
<span data-ttu-id="eea6e-103">Удаляет управляемую учетную запись хранилища Azure с основным хранилищем и все связанные определения SAS.</span><span class="sxs-lookup"><span data-stu-id="eea6e-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="eea6e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eea6e-104">SYNTAX</span></span>

### <span data-ttu-id="eea6e-105">ByDefinitionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eea6e-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea6e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eea6e-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eea6e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eea6e-107">DESCRIPTION</span></span>
<span data-ttu-id="eea6e-108">Отменяет связь учетной записи хранения Azure из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="eea6e-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="eea6e-109">Это не приведет к удалению учетной записи хранения Azure, но удаляет ключи учетной записи из управления с помощью Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="eea6e-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="eea6e-110">Также удаляются все связанные определения SAS хранилища управляемых хранилищ.</span><span class="sxs-lookup"><span data-stu-id="eea6e-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="eea6e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eea6e-111">EXAMPLES</span></span>

### <span data-ttu-id="eea6e-112">Пример 1: Удаление учетной записи хранения для хранилища ключей, управляемой службой хранилища Azure, и всех связанных определений SAS.</span><span class="sxs-lookup"><span data-stu-id="eea6e-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
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

<span data-ttu-id="eea6e-113">Отменяет связь учетной записи хранилища Azure "mystorageaccount" с основным хранилищем "myvault" и останавливает управление ключами из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="eea6e-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="eea6e-114">Учетная запись "mystorageaccount" не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="eea6e-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="eea6e-115">Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="eea6e-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="eea6e-116">Пример 2: Удаление учетной записи хранения для хранилища ключей в службе управления правами и всех связанных определений SAS без подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="eea6e-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
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

<span data-ttu-id="eea6e-117">Отменяет связь учетной записи хранилища Azure "mystorageaccount" с основным хранилищем "myvault" и останавливает управление ключами из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="eea6e-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="eea6e-118">Учетная запись "mystorageaccount" не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="eea6e-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="eea6e-119">Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="eea6e-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="eea6e-120">Пример 3: окончательное удаление (удаление) учетной записи хранения для хранилища ключей, управляемой хранилищем Azure, и всех связанных определений SAS из хранилища с возможностью удаления с мягким удалением.</span><span class="sxs-lookup"><span data-stu-id="eea6e-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="eea6e-121">В этом примере предполагается, что для этого хранилища включено мягкое удаление.</span><span class="sxs-lookup"><span data-stu-id="eea6e-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="eea6e-122">Убедитесь, что это так, проверив свойства хранилища или атрибут RecoveryLevel сущности в хранилище.</span><span class="sxs-lookup"><span data-stu-id="eea6e-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="eea6e-123">Первый командлет разрывает учетную запись хранилища Azure "mystorageaccount" из хранилища ключей "myvault" и останавливает управление ключами с помощью основного хранилища.</span><span class="sxs-lookup"><span data-stu-id="eea6e-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="eea6e-124">Учетная запись "mystorageaccount" не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="eea6e-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="eea6e-125">Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="eea6e-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="eea6e-126">Второй командлет удостоверяется в том, что учетная запись хранения находится в удаленном состоянии, но может быть восстановлено.</span><span class="sxs-lookup"><span data-stu-id="eea6e-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="eea6e-127">Для достижения этого состояния может потребоваться некоторое время. Разрешите ~ 30S перед тем, как попытаться.</span><span class="sxs-lookup"><span data-stu-id="eea6e-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="eea6e-128">Третий командлет окончательно удаляет учетную запись хранения, после чего восстановление больше невозможно.</span><span class="sxs-lookup"><span data-stu-id="eea6e-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="eea6e-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eea6e-129">PARAMETERS</span></span>

### <span data-ttu-id="eea6e-130">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="eea6e-130">-AccountName</span></span>
<span data-ttu-id="eea6e-131">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="eea6e-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="eea6e-132">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="eea6e-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="eea6e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea6e-133">-DefaultProfile</span></span>
<span data-ttu-id="eea6e-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eea6e-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eea6e-135">-Force</span><span class="sxs-lookup"><span data-stu-id="eea6e-135">-Force</span></span>
<span data-ttu-id="eea6e-136">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="eea6e-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eea6e-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eea6e-137">-InputObject</span></span>
<span data-ttu-id="eea6e-138">Объект ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="eea6e-138">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="eea6e-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="eea6e-139">-InRemovedState</span></span>
<span data-ttu-id="eea6e-140">Окончательное удаление прежней управляемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="eea6e-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="eea6e-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eea6e-141">-PassThru</span></span>
<span data-ttu-id="eea6e-142">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="eea6e-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="eea6e-143">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="eea6e-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="eea6e-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="eea6e-144">-VaultName</span></span>
<span data-ttu-id="eea6e-145">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="eea6e-145">Vault name.</span></span>
<span data-ttu-id="eea6e-146">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="eea6e-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="eea6e-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eea6e-147">-Confirm</span></span>
<span data-ttu-id="eea6e-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eea6e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea6e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea6e-149">-WhatIf</span></span>
<span data-ttu-id="eea6e-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eea6e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea6e-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eea6e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea6e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea6e-152">CommonParameters</span></span>
<span data-ttu-id="eea6e-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eea6e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea6e-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eea6e-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea6e-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eea6e-155">INPUTS</span></span>

### <span data-ttu-id="eea6e-156">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="eea6e-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="eea6e-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eea6e-157">OUTPUTS</span></span>

### <span data-ttu-id="eea6e-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eea6e-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="eea6e-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="eea6e-159">NOTES</span></span>

## <span data-ttu-id="eea6e-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eea6e-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

