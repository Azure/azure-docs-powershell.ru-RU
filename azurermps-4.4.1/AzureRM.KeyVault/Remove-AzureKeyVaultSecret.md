---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: e5ec1e2377b9a1c04fc10ce976bd800227baabed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568054"
---
# <span data-ttu-id="a16a3-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a16a3-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="a16a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a16a3-102">SYNOPSIS</span></span>
<span data-ttu-id="a16a3-103">Удаление секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="a16a3-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a16a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a16a3-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a16a3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a16a3-105">DESCRIPTION</span></span>
<span data-ttu-id="a16a3-106">Командлет Remove-AzureKeyVaultSecret удаляет секрет из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a16a3-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="a16a3-107">Если секрет был случайно удален, его можно восстановить с помощью Undo-AzureKeyVaultSecretRemoval пользователем с особыми разрешениями на восстановление.</span><span class="sxs-lookup"><span data-stu-id="a16a3-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="a16a3-108">Этот командлет имеет значение High для свойства **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="a16a3-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="a16a3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a16a3-109">EXAMPLES</span></span>

### <span data-ttu-id="a16a3-110">Пример 1: удаление секрета из хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="a16a3-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="a16a3-111">Эта команда удаляет секрет с именем FinanceSecret из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="a16a3-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="a16a3-112">Пример 2: удаление секрета из хранилища ключей без подтверждения пользователя</span><span class="sxs-lookup"><span data-stu-id="a16a3-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="a16a3-113">Эта команда удаляет секрет с именем FinanceSecret из хранилища ключей, именуемого contoso.</span><span class="sxs-lookup"><span data-stu-id="a16a3-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="a16a3-114">Команда определяет параметры *Force* и *Confirm* , поэтому командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a16a3-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a16a3-115">Пример 3: Удаление удаленного секрета из хранилища ключей без возможности восстановления</span><span class="sxs-lookup"><span data-stu-id="a16a3-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="a16a3-116">Эта команда перемещает секрет с именем FinanceSecret из хранилища ключей Contoso без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="a16a3-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="a16a3-117">Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a16a3-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="a16a3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a16a3-118">PARAMETERS</span></span>

### <span data-ttu-id="a16a3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a16a3-119">-Force</span></span>
<span data-ttu-id="a16a3-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a16a3-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a16a3-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a16a3-121">-InRemovedState</span></span>
<span data-ttu-id="a16a3-122">Если он указан, окончательно удаляет ранее удаленный секрет.</span><span class="sxs-lookup"><span data-stu-id="a16a3-122">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="a16a3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a16a3-123">-Name</span></span>
<span data-ttu-id="a16a3-124">Указывает имя секрета.</span><span class="sxs-lookup"><span data-stu-id="a16a3-124">Specifies the name of a secret.</span></span>
<span data-ttu-id="a16a3-125">Этот командлет создает полное доменное имя (FQDN) для секрета на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="a16a3-125">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a16a3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a16a3-126">-PassThru</span></span>
<span data-ttu-id="a16a3-127">Указывает на то, что этот командлет возвращает объект **Microsoft. Azure. Commands. KeyVault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="a16a3-127">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="a16a3-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a16a3-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a16a3-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a16a3-129">-VaultName</span></span>
<span data-ttu-id="a16a3-130">Указывает имя хранилища ключей, к которому относится секрет.</span><span class="sxs-lookup"><span data-stu-id="a16a3-130">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="a16a3-131">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="a16a3-131">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a16a3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a16a3-132">-Confirm</span></span>
<span data-ttu-id="a16a3-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a16a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a16a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a16a3-134">-WhatIf</span></span>
<span data-ttu-id="a16a3-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a16a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a16a3-136">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a16a3-136">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a16a3-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a16a3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a16a3-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16a3-138">-DefaultProfile</span></span>
<span data-ttu-id="a16a3-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a16a3-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a16a3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16a3-140">CommonParameters</span></span>
<span data-ttu-id="a16a3-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a16a3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16a3-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a16a3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16a3-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a16a3-143">INPUTS</span></span>

### <span data-ttu-id="a16a3-144">Подстрок</span><span class="sxs-lookup"><span data-stu-id="a16a3-144">String</span></span>

## <span data-ttu-id="a16a3-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a16a3-145">OUTPUTS</span></span>

### <span data-ttu-id="a16a3-146">Microsoft. Azure. Commands. KeyVault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="a16a3-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="a16a3-147">Этот командлет возвращает значение только в том случае, если указан параметр *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="a16a3-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="a16a3-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="a16a3-148">NOTES</span></span>

## <span data-ttu-id="a16a3-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a16a3-149">RELATED LINKS</span></span>

[<span data-ttu-id="a16a3-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a16a3-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="a16a3-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a16a3-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="a16a3-152">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="a16a3-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

