---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 71a0dcebdc889eb8116089eb3c5a5b8379c72b20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243352"
---
# <span data-ttu-id="b1f86-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b1f86-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="b1f86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1f86-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f86-103">Удаляет секрет в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="b1f86-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="b1f86-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1f86-104">SYNTAX</span></span>

### <span data-ttu-id="b1f86-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1f86-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1f86-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b1f86-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1f86-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1f86-107">DESCRIPTION</span></span>
<span data-ttu-id="b1f86-108">Новый Remove-AzKeyVaultSecret удаляет секрет в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="b1f86-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="b1f86-109">Если секрет был случайно удален, его можно восстановить с помощью Undo-AzKeyVaultSecretRemoval пользователя со специальными разрешениями на восстановление.</span><span class="sxs-lookup"><span data-stu-id="b1f86-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="b1f86-110">Этот cmdlet имеет высокое значение для свойства **ConfirmImpact.**</span><span class="sxs-lookup"><span data-stu-id="b1f86-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="b1f86-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1f86-111">EXAMPLES</span></span>

### <span data-ttu-id="b1f86-112">Пример 1. Удаление секрета из сейфа ключа</span><span class="sxs-lookup"><span data-stu-id="b1f86-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="b1f86-113">Эта команда удаляет секретную службу FinanceSecret из хранилища ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="b1f86-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="b1f86-114">Пример 2. Удаление секрета из сейфа ключа без подтверждения пользователем</span><span class="sxs-lookup"><span data-stu-id="b1f86-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="b1f86-115">Эта команда удаляет секретную службу FinanceSecret из хранилища ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="b1f86-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="b1f86-116">Эта команда определяет параметры *Force* и *Confirm,* поэтому командлет не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b1f86-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="b1f86-117">Пример 3. Окончательное удаление секрета из сейфа ключа</span><span class="sxs-lookup"><span data-stu-id="b1f86-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="b1f86-118">Эта команда окончательно перетаскирует секретную службу FinanceSecret из ключного сейфа Contoso.</span><span class="sxs-lookup"><span data-stu-id="b1f86-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="b1f86-119">Для выполнения этого cmdlet необходимо разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b1f86-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="b1f86-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1f86-120">PARAMETERS</span></span>

### <span data-ttu-id="b1f86-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f86-121">-DefaultProfile</span></span>
<span data-ttu-id="b1f86-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b1f86-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1f86-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b1f86-123">-Force</span></span>
<span data-ttu-id="b1f86-124">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b1f86-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1f86-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1f86-125">-InputObject</span></span>
<span data-ttu-id="b1f86-126">Key Vault Secret Object</span><span class="sxs-lookup"><span data-stu-id="b1f86-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f86-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b1f86-127">-InRemovedState</span></span>
<span data-ttu-id="b1f86-128">Если она есть, удаляет удаленную секретную навсегда.</span><span class="sxs-lookup"><span data-stu-id="b1f86-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="b1f86-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b1f86-129">-Name</span></span>
<span data-ttu-id="b1f86-130">Указывает имя секрета.</span><span class="sxs-lookup"><span data-stu-id="b1f86-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="b1f86-131">Этот cmdlet конструирует полное доменное имя секретного домена на основе имени, указанного этим параметром, имени сейфа ключа и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="b1f86-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1f86-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1f86-132">-PassThru</span></span>
<span data-ttu-id="b1f86-133">Указывает на то, что этот командлет возвращает **объект Microsoft.Azure.Commands.KeyVault.Models.Secret.**</span><span class="sxs-lookup"><span data-stu-id="b1f86-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="b1f86-134">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b1f86-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1f86-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b1f86-135">-VaultName</span></span>
<span data-ttu-id="b1f86-136">Указывает имя ключного сейфа, к которому относится секрет.</span><span class="sxs-lookup"><span data-stu-id="b1f86-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="b1f86-137">Этот cmdlet конструирует FQDN ключа хранилища на основе имени, указанного этим параметром, и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="b1f86-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="b1f86-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1f86-138">-Confirm</span></span>
<span data-ttu-id="b1f86-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f86-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f86-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f86-140">-WhatIf</span></span>
<span data-ttu-id="b1f86-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f86-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1f86-142">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f86-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1f86-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b1f86-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f86-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f86-144">CommonParameters</span></span>
<span data-ttu-id="b1f86-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f86-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f86-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1f86-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f86-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1f86-147">INPUTS</span></span>

### <span data-ttu-id="b1f86-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b1f86-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="b1f86-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1f86-149">OUTPUTS</span></span>

### <span data-ttu-id="b1f86-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b1f86-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="b1f86-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1f86-151">NOTES</span></span>

## <span data-ttu-id="b1f86-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1f86-152">RELATED LINKS</span></span>

[<span data-ttu-id="b1f86-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b1f86-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="b1f86-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b1f86-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="b1f86-155">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="b1f86-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

