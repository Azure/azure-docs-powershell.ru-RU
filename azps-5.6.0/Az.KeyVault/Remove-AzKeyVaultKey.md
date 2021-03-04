---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 0d458d6063aa530b1f30f6a79244e7d719080bf6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952520"
---
# <span data-ttu-id="96dba-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96dba-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="96dba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96dba-102">SYNOPSIS</span></span>
<span data-ttu-id="96dba-103">Удаляет ключ в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="96dba-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="96dba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="96dba-104">SYNTAX</span></span>

### <span data-ttu-id="96dba-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96dba-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96dba-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="96dba-106">HsmByVaultName</span></span>
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96dba-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="96dba-107">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96dba-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96dba-108">DESCRIPTION</span></span>
<span data-ttu-id="96dba-109">Новый Remove-AzKeyVaultKey удаляет ключ из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="96dba-109">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="96dba-110">Если ключ был случайно удален, его можно восстановить с помощью Undo-AzKeyVaultKeyRemoval пользователей со специальными разрешениями на восстановление.</span><span class="sxs-lookup"><span data-stu-id="96dba-110">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="96dba-111">Этот cmdlet имеет высокое значение для свойства **ConfirmImpact.**</span><span class="sxs-lookup"><span data-stu-id="96dba-111">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="96dba-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="96dba-112">EXAMPLES</span></span>

### <span data-ttu-id="96dba-113">Пример 1. Удаление ключа из хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="96dba-113">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="96dba-114">Эта команда удаляет ключ ITSoftware из хранилища ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="96dba-114">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="96dba-115">Пример 2. Удаление ключа без подтверждения пользователем</span><span class="sxs-lookup"><span data-stu-id="96dba-115">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="96dba-116">Эта команда удаляет ключ ITSoftware из хранилища ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="96dba-116">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="96dba-117">Эта команда определяет параметр *Force,* поэтому командлет не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="96dba-117">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="96dba-118">Пример 3. Окончательное удаление удаленного ключа из хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="96dba-118">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="96dba-119">Эта команда окончательно удаляет ключ ITSoftware из хранилища с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="96dba-119">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="96dba-120">Для выполнения этого cmdlet необходимо разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="96dba-120">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="96dba-121">Пример 4. Удаление ключей с помощью оператора конвейера</span><span class="sxs-lookup"><span data-stu-id="96dba-121">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="96dba-122">Эта команда получает все ключи в хранилище ключей Contoso и передает их в командлет **Where-Object** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="96dba-122">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="96dba-123">Этот cmdlet передает текущему $False, которые имеют значение $False **Enabled.**</span><span class="sxs-lookup"><span data-stu-id="96dba-123">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="96dba-124">Этот cmdlet удаляет эти клавиши.</span><span class="sxs-lookup"><span data-stu-id="96dba-124">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="96dba-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96dba-125">PARAMETERS</span></span>

### <span data-ttu-id="96dba-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96dba-126">-DefaultProfile</span></span>
<span data-ttu-id="96dba-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="96dba-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96dba-128">-Force</span><span class="sxs-lookup"><span data-stu-id="96dba-128">-Force</span></span>
<span data-ttu-id="96dba-129">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="96dba-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96dba-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="96dba-130">-HsmName</span></span>
<span data-ttu-id="96dba-131">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="96dba-131">HSM name.</span></span> <span data-ttu-id="96dba-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="96dba-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96dba-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96dba-133">-InputObject</span></span>
<span data-ttu-id="96dba-134">Объект KeyBundle</span><span class="sxs-lookup"><span data-stu-id="96dba-134">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96dba-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="96dba-135">-InRemovedState</span></span>
<span data-ttu-id="96dba-136">Удалите ранее удаленный ключ навсегда.</span><span class="sxs-lookup"><span data-stu-id="96dba-136">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="96dba-137">-Name</span><span class="sxs-lookup"><span data-stu-id="96dba-137">-Name</span></span>
<span data-ttu-id="96dba-138">Указывает имя ключа, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="96dba-138">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="96dba-139">Этот проектлет определяет полное доменное имя ключа на основе имени, указанного этим параметром, имени хранилища ключа и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="96dba-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96dba-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96dba-140">-PassThru</span></span>
<span data-ttu-id="96dba-141">Указывает на то, что этот командлет возвращает объект **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="96dba-141">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="96dba-142">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="96dba-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="96dba-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="96dba-143">-VaultName</span></span>
<span data-ttu-id="96dba-144">Указывает имя хранилища ключей, из которого нужно удалить ключ.</span><span class="sxs-lookup"><span data-stu-id="96dba-144">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="96dba-145">Этот cmdlet конструирует FQDN ключа хранилища на основе имени, указанного этим параметром, и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="96dba-145">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96dba-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96dba-146">-Confirm</span></span>
<span data-ttu-id="96dba-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="96dba-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96dba-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96dba-148">-WhatIf</span></span>
<span data-ttu-id="96dba-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96dba-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96dba-150">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96dba-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96dba-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="96dba-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96dba-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96dba-152">CommonParameters</span></span>
<span data-ttu-id="96dba-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96dba-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96dba-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96dba-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96dba-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96dba-155">INPUTS</span></span>

### <span data-ttu-id="96dba-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="96dba-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="96dba-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="96dba-157">OUTPUTS</span></span>

### <span data-ttu-id="96dba-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96dba-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="96dba-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="96dba-159">NOTES</span></span>

## <span data-ttu-id="96dba-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96dba-160">RELATED LINKS</span></span>

[<span data-ttu-id="96dba-161">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96dba-161">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="96dba-162">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96dba-162">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="96dba-163">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="96dba-163">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="96dba-164">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="96dba-164">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

