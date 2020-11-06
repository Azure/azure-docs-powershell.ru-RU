---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: bff9c08a0c36fb7a4d89fb86d9c219491f3642b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564407"
---
# <span data-ttu-id="17786-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17786-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="17786-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17786-102">SYNOPSIS</span></span>
<span data-ttu-id="17786-103">Удаление секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="17786-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17786-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17786-104">SYNTAX</span></span>

### <span data-ttu-id="17786-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17786-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17786-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="17786-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17786-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17786-107">DESCRIPTION</span></span>
<span data-ttu-id="17786-108">Командлет Remove-AzureKeyVaultSecret удаляет секрет из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="17786-108">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="17786-109">Если секрет был случайно удален, его можно восстановить с помощью Undo-AzureKeyVaultSecretRemoval пользователем с особыми разрешениями на восстановление.</span><span class="sxs-lookup"><span data-stu-id="17786-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="17786-110">Этот командлет имеет значение High для свойства **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="17786-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="17786-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17786-111">EXAMPLES</span></span>

### <span data-ttu-id="17786-112">Пример 1: удаление секрета из хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="17786-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

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

<span data-ttu-id="17786-113">Эта команда удаляет секрет с именем FinanceSecret из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="17786-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="17786-114">Пример 2: удаление секрета из хранилища ключей без подтверждения пользователя</span><span class="sxs-lookup"><span data-stu-id="17786-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

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

<span data-ttu-id="17786-115">Эта команда удаляет секрет с именем FinanceSecret из хранилища ключей, именуемого contoso.</span><span class="sxs-lookup"><span data-stu-id="17786-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="17786-116">Команда определяет параметры *Force* и *Confirm* , поэтому командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="17786-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="17786-117">Пример 3: Удаление удаленного секрета из хранилища ключей без возможности восстановления</span><span class="sxs-lookup"><span data-stu-id="17786-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="17786-118">Эта команда перемещает секрет с именем FinanceSecret из хранилища ключей Contoso без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="17786-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="17786-119">Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="17786-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="17786-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17786-120">PARAMETERS</span></span>

### <span data-ttu-id="17786-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17786-121">-DefaultProfile</span></span>
<span data-ttu-id="17786-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="17786-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17786-123">-Force</span><span class="sxs-lookup"><span data-stu-id="17786-123">-Force</span></span>
<span data-ttu-id="17786-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="17786-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17786-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17786-125">-InputObject</span></span>
<span data-ttu-id="17786-126">Секретный объект, защищенный основным хранилищем</span><span class="sxs-lookup"><span data-stu-id="17786-126">Key Vault Secret Object</span></span>

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

### <span data-ttu-id="17786-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="17786-127">-InRemovedState</span></span>
<span data-ttu-id="17786-128">Если он указан, окончательно удаляет ранее удаленный секрет.</span><span class="sxs-lookup"><span data-stu-id="17786-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="17786-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="17786-129">-Name</span></span>
<span data-ttu-id="17786-130">Указывает имя секрета.</span><span class="sxs-lookup"><span data-stu-id="17786-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="17786-131">Этот командлет создает полное доменное имя (FQDN) для секрета на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="17786-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="17786-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17786-132">-PassThru</span></span>
<span data-ttu-id="17786-133">Указывает на то, что этот командлет возвращает объект **Microsoft. Azure. Commands. KeyVault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="17786-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="17786-134">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="17786-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="17786-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="17786-135">-VaultName</span></span>
<span data-ttu-id="17786-136">Указывает имя хранилища ключей, к которому относится секрет.</span><span class="sxs-lookup"><span data-stu-id="17786-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="17786-137">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="17786-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="17786-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17786-138">-Confirm</span></span>
<span data-ttu-id="17786-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17786-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17786-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17786-140">-WhatIf</span></span>
<span data-ttu-id="17786-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17786-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17786-142">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17786-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17786-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17786-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17786-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17786-144">CommonParameters</span></span>
<span data-ttu-id="17786-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17786-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17786-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17786-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17786-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17786-147">INPUTS</span></span>

### <span data-ttu-id="17786-148">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="17786-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="17786-149">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="17786-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="17786-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17786-150">OUTPUTS</span></span>

### <span data-ttu-id="17786-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17786-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="17786-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="17786-152">NOTES</span></span>

## <span data-ttu-id="17786-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17786-153">RELATED LINKS</span></span>

[<span data-ttu-id="17786-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17786-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="17786-155">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17786-155">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="17786-156">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="17786-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

