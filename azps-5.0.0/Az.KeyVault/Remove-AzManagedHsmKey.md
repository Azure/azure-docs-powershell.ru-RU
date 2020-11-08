---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245289"
---
# <span data-ttu-id="bcdec-101">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="bcdec-101">Remove-AzManagedHsmKey</span></span>

## <span data-ttu-id="bcdec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bcdec-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdec-103">Удаление ключа в управляемом HSM.</span><span class="sxs-lookup"><span data-stu-id="bcdec-103">Deletes a key in a managed HSM.</span></span>

## <span data-ttu-id="bcdec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bcdec-104">SYNTAX</span></span>

### <span data-ttu-id="bcdec-105">RemoveByKeyNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bcdec-105">RemoveByKeyNameParameterSet (Default)</span></span>
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcdec-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcdec-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcdec-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcdec-107">DESCRIPTION</span></span>
<span data-ttu-id="bcdec-108">Командлет Remove-AzManagedHsmKey удаляет ключ из управляемого HSM-ключа.</span><span class="sxs-lookup"><span data-stu-id="bcdec-108">The Remove-AzManagedHsmKey cmdlet deletes a key in a managed HSM.</span></span>
<span data-ttu-id="bcdec-109">Если клавиша была случайно удалена, ключ может быть восстановлен с помощью Undo-AzManagedHsmKeyRemoval пользователем, у которого есть особые разрешения на восстановление.</span><span class="sxs-lookup"><span data-stu-id="bcdec-109">If the key was accidentally deleted the key can be recovered using Undo-AzManagedHsmKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="bcdec-110">Этот командлет имеет значение High для свойства **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="bcdec-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="bcdec-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bcdec-111">EXAMPLES</span></span>

### <span data-ttu-id="bcdec-112">Пример 1: Удаление ключа из управляемого HSM-кода</span><span class="sxs-lookup"><span data-stu-id="bcdec-112">Example 1: Remove a key from a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="bcdec-113">Эта команда удаляет ключ с именем TestKey из управляемого HSM, именуемого testmhsm.</span><span class="sxs-lookup"><span data-stu-id="bcdec-113">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="bcdec-114">Пример 2: Удаление ключа без подтверждения пользователя</span><span class="sxs-lookup"><span data-stu-id="bcdec-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

<span data-ttu-id="bcdec-115">Эта команда удаляет ключ с именем TestKey из управляемого HSM, именуемого testmhsm.</span><span class="sxs-lookup"><span data-stu-id="bcdec-115">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>
<span data-ttu-id="bcdec-116">Команда задает параметр *Force* и, следовательно, командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bcdec-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="bcdec-117">Пример 3: Удаление удаленного ключа из управляемого HSM-кода без возможности восстановления</span><span class="sxs-lookup"><span data-stu-id="bcdec-117">Example 3: Purge a deleted key from the managed HSM permanently</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

<span data-ttu-id="bcdec-118">Эта команда удаляет ключ с именем TestKey из управляемого HSM, именуемого testmhsm, без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="bcdec-118">This command removes the key named testkey from the managed HSM named testmhsm permanently.</span></span>
<span data-ttu-id="bcdec-119">Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого управляемого HSM.</span><span class="sxs-lookup"><span data-stu-id="bcdec-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this managed HSM.</span></span>

### <span data-ttu-id="bcdec-120">Пример 4: Удаление ключей с помощью оператора Pipeline</span><span class="sxs-lookup"><span data-stu-id="bcdec-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

<span data-ttu-id="bcdec-121">Эта команда получает все ключи в управляемом HSM-приложении с именем testmhsm и передает их в командлет **Where – Object** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="bcdec-121">This command gets all the keys in the managed HSM named testmhsm and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bcdec-122">Этот командлет передает ключи со значением $False для атрибута **Enabled** для текущего командлета.</span><span class="sxs-lookup"><span data-stu-id="bcdec-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="bcdec-123">Этот командлет удаляет эти ключи.</span><span class="sxs-lookup"><span data-stu-id="bcdec-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="bcdec-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bcdec-124">PARAMETERS</span></span>

### <span data-ttu-id="bcdec-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdec-125">-DefaultProfile</span></span>
<span data-ttu-id="bcdec-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdec-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcdec-127">-Force</span><span class="sxs-lookup"><span data-stu-id="bcdec-127">-Force</span></span>
<span data-ttu-id="bcdec-128">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bcdec-128">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bcdec-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="bcdec-129">-HsmName</span></span>
<span data-ttu-id="bcdec-130">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="bcdec-130">HSM name.</span></span> <span data-ttu-id="bcdec-131">Командлет создает полное доменное имя управляемого HSM-файла на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="bcdec-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdec-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcdec-132">-InputObject</span></span>
<span data-ttu-id="bcdec-133">Объект Key</span><span class="sxs-lookup"><span data-stu-id="bcdec-133">Key Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcdec-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="bcdec-134">-InRemovedState</span></span>
<span data-ttu-id="bcdec-135">Удаление ранее удаленного ключа без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="bcdec-135">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="bcdec-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bcdec-136">-Name</span></span>
<span data-ttu-id="bcdec-137">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="bcdec-137">Key name.</span></span>
<span data-ttu-id="bcdec-138">Командлет конструирует полное доменное имя ключа из управляемого имени HSM, в настоящее время выбранной среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="bcdec-138">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdec-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcdec-139">-PassThru</span></span>
<span data-ttu-id="bcdec-140">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="bcdec-140">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bcdec-141">Если указан этот параметр, командлет возвращает объект ключа, который был удален.</span><span class="sxs-lookup"><span data-stu-id="bcdec-141">If this switch is specified, the cmdlet returns the key object that was deleted.</span></span>

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

### <span data-ttu-id="bcdec-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcdec-142">-Confirm</span></span>
<span data-ttu-id="bcdec-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bcdec-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcdec-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcdec-144">-WhatIf</span></span>
<span data-ttu-id="bcdec-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bcdec-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcdec-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bcdec-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcdec-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdec-147">CommonParameters</span></span>
<span data-ttu-id="bcdec-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bcdec-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdec-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcdec-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdec-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bcdec-150">INPUTS</span></span>

### <span data-ttu-id="bcdec-151">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bcdec-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="bcdec-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcdec-152">OUTPUTS</span></span>

### <span data-ttu-id="bcdec-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bcdec-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="bcdec-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="bcdec-154">NOTES</span></span>

## <span data-ttu-id="bcdec-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcdec-155">RELATED LINKS</span></span>

[<span data-ttu-id="bcdec-156">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="bcdec-156">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="bcdec-157">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="bcdec-157">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="bcdec-158">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="bcdec-158">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="bcdec-159">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="bcdec-159">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="bcdec-160">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="bcdec-160">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="bcdec-161">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="bcdec-161">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)