---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 3c5435d1a472341d0447ead2f384fa892d6e1202
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404485"
---
# <span data-ttu-id="e4671-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e4671-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="e4671-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4671-102">SYNOPSIS</span></span>
<span data-ttu-id="e4671-103">Удаляет ключ в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="e4671-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="e4671-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e4671-104">SYNTAX</span></span>

### <span data-ttu-id="e4671-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4671-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4671-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="e4671-106">HsmByVaultName</span></span>
```
Remove-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4671-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e4671-107">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4671-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4671-108">DESCRIPTION</span></span>
<span data-ttu-id="e4671-109">С Remove-AzKeyVaultKey- и клавиши удаляются из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="e4671-109">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="e4671-110">Если ключ был случайно удален, его можно восстановить с помощью Undo-AzKeyVaultKeyRemoval пользователей со специальными разрешениями на восстановление.</span><span class="sxs-lookup"><span data-stu-id="e4671-110">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="e4671-111">Этот cmdlet имеет высокое значение для свойства **ConfirmImpact.**</span><span class="sxs-lookup"><span data-stu-id="e4671-111">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="e4671-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e4671-112">EXAMPLES</span></span>

### <span data-ttu-id="e4671-113">Пример 1. Удаление ключа из хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="e4671-113">Example 1: Remove a key from a key vault</span></span>
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

<span data-ttu-id="e4671-114">Эта команда удаляет ключ ITSoftware из хранилища ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="e4671-114">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="e4671-115">Пример 2. Удаление ключа без подтверждения пользователем</span><span class="sxs-lookup"><span data-stu-id="e4671-115">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="e4671-116">Эта команда удаляет ключ ITSoftware из хранилища ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="e4671-116">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="e4671-117">Эта команда определяет параметр *Force,* поэтому командлет не будет запросить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e4671-117">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e4671-118">Пример 3. Окончательное удаление удаленного ключа из хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="e4671-118">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="e4671-119">Эта команда окончательно удаляет ключ ITSoftware из хранилища с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="e4671-119">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="e4671-120">Для выполнения этого cmdlet необходимо разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="e4671-120">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="e4671-121">Пример 4. Удаление ключей с помощью оператора конвейера</span><span class="sxs-lookup"><span data-stu-id="e4671-121">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="e4671-122">Эта команда получает все ключи в хранилище ключей Contoso и передает их в командлет **Where-Object** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="e4671-122">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e4671-123">Этот cmdlet передает текущему $False, которые имеют значение $False **Enabled.**</span><span class="sxs-lookup"><span data-stu-id="e4671-123">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="e4671-124">Этот cmdlet удаляет эти клавиши.</span><span class="sxs-lookup"><span data-stu-id="e4671-124">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="e4671-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4671-125">PARAMETERS</span></span>

### <span data-ttu-id="e4671-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4671-126">-DefaultProfile</span></span>
<span data-ttu-id="e4671-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e4671-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4671-128">-Force</span><span class="sxs-lookup"><span data-stu-id="e4671-128">-Force</span></span>
<span data-ttu-id="e4671-129">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e4671-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4671-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="e4671-130">-HsmName</span></span>
<span data-ttu-id="e4671-131">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="e4671-131">HSM name.</span></span> <span data-ttu-id="e4671-132">С его учетом именем и выбранной средой строится FQDN управляемой HSM- среды.</span><span class="sxs-lookup"><span data-stu-id="e4671-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e4671-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4671-133">-InputObject</span></span>
<span data-ttu-id="e4671-134">Объект KeyBundle</span><span class="sxs-lookup"><span data-stu-id="e4671-134">KeyBundle Object</span></span>

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

### <span data-ttu-id="e4671-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e4671-135">-InRemovedState</span></span>
<span data-ttu-id="e4671-136">Удалите ранее удаленный ключ навсегда.</span><span class="sxs-lookup"><span data-stu-id="e4671-136">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="e4671-137">-Name</span><span class="sxs-lookup"><span data-stu-id="e4671-137">-Name</span></span>
<span data-ttu-id="e4671-138">Указывает имя ключа, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e4671-138">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="e4671-139">Этот cmdlet конструирует полное доменное имя (FQDN) ключа на основе имени, указанного этим параметром, имени хранилища ключа и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="e4671-139">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="e4671-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4671-140">-PassThru</span></span>
<span data-ttu-id="e4671-141">Указывает на то, что этот командлет возвращает объект **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="e4671-141">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="e4671-142">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e4671-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4671-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e4671-143">-VaultName</span></span>
<span data-ttu-id="e4671-144">Указывает имя хранилища ключей, из которого нужно удалить ключ.</span><span class="sxs-lookup"><span data-stu-id="e4671-144">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="e4671-145">Этот cmdlet конструирует FQDN ключа хранилища на основе имени, указанного этим параметром, и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="e4671-145">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="e4671-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4671-146">-Confirm</span></span>
<span data-ttu-id="e4671-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e4671-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4671-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4671-148">-WhatIf</span></span>
<span data-ttu-id="e4671-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4671-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4671-150">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4671-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4671-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e4671-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4671-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4671-152">CommonParameters</span></span>
<span data-ttu-id="e4671-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4671-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4671-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4671-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4671-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4671-155">INPUTS</span></span>

### <span data-ttu-id="e4671-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e4671-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="e4671-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4671-157">OUTPUTS</span></span>

### <span data-ttu-id="e4671-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e4671-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="e4671-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e4671-159">NOTES</span></span>

## <span data-ttu-id="e4671-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4671-160">RELATED LINKS</span></span>

[<span data-ttu-id="e4671-161">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e4671-161">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="e4671-162">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e4671-162">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)


[<span data-ttu-id="e4671-163">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="e4671-163">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

