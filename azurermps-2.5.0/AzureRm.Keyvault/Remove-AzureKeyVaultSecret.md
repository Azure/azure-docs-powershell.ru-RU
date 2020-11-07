---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 56cc6b11c517379f1d13ebe2dbf2cee00f18211b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913332"
---
# <span data-ttu-id="8cda9-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8cda9-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="8cda9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cda9-102">SYNOPSIS</span></span>
<span data-ttu-id="8cda9-103">Удаление секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8cda9-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cda9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cda9-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cda9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cda9-105">DESCRIPTION</span></span>
<span data-ttu-id="8cda9-106">Командлет Remove-AzureKeyVaultSecret удаляет секрет из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cda9-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="8cda9-107">Если секрет был случайно удален, его можно восстановить с помощью Undo-AzureKeyVaultSecretRemoval пользователем с особыми разрешениями на восстановление.</span><span class="sxs-lookup"><span data-stu-id="8cda9-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="8cda9-108">Этот командлет имеет значение High для свойства **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="8cda9-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="8cda9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cda9-109">EXAMPLES</span></span>

### <span data-ttu-id="8cda9-110">Пример 1: удаление секрета из хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="8cda9-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="8cda9-111">Эта команда удаляет секрет с именем FinanceSecret из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="8cda9-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="8cda9-112">Пример 2: удаление секрета из хранилища ключей без подтверждения пользователя</span><span class="sxs-lookup"><span data-stu-id="8cda9-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="8cda9-113">Эта команда удаляет секрет с именем FinanceSecret из хранилища ключей, именуемого contoso.</span><span class="sxs-lookup"><span data-stu-id="8cda9-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="8cda9-114">Команда определяет параметры *Force* и *Confirm* , поэтому командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="8cda9-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8cda9-115">Пример 3: Удаление удаленного секрета из хранилища ключей без возможности восстановления</span><span class="sxs-lookup"><span data-stu-id="8cda9-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="8cda9-116">Эта команда перемещает секрет с именем FinanceSecret из хранилища ключей Contoso без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="8cda9-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="8cda9-117">Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cda9-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="8cda9-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cda9-118">PARAMETERS</span></span>

### <span data-ttu-id="8cda9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cda9-119">-DefaultProfile</span></span>
<span data-ttu-id="8cda9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8cda9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cda9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8cda9-121">-Force</span></span>
<span data-ttu-id="8cda9-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8cda9-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cda9-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8cda9-123">-InRemovedState</span></span>
<span data-ttu-id="8cda9-124">Если он указан, окончательно удаляет ранее удаленный секрет.</span><span class="sxs-lookup"><span data-stu-id="8cda9-124">If present, removes the previously deleted secret permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cda9-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8cda9-125">-Name</span></span>
<span data-ttu-id="8cda9-126">Указывает имя секрета.</span><span class="sxs-lookup"><span data-stu-id="8cda9-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="8cda9-127">Этот командлет создает полное доменное имя (FQDN) для секрета на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="8cda9-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cda9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cda9-128">-PassThru</span></span>
<span data-ttu-id="8cda9-129">Указывает на то, что этот командлет возвращает объект **Microsoft. Azure. Commands. KeyVault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="8cda9-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="8cda9-130">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8cda9-130">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cda9-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8cda9-131">-VaultName</span></span>
<span data-ttu-id="8cda9-132">Указывает имя хранилища ключей, к которому относится секрет.</span><span class="sxs-lookup"><span data-stu-id="8cda9-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="8cda9-133">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="8cda9-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cda9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cda9-134">-Confirm</span></span>
<span data-ttu-id="8cda9-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8cda9-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cda9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cda9-136">-WhatIf</span></span>
<span data-ttu-id="8cda9-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8cda9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cda9-138">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8cda9-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cda9-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8cda9-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cda9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cda9-140">CommonParameters</span></span>
<span data-ttu-id="8cda9-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8cda9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cda9-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cda9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cda9-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cda9-143">INPUTS</span></span>

### <span data-ttu-id="8cda9-144">Подстрок</span><span class="sxs-lookup"><span data-stu-id="8cda9-144">String</span></span>

## <span data-ttu-id="8cda9-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cda9-145">OUTPUTS</span></span>

### <span data-ttu-id="8cda9-146">Microsoft. Azure. Commands. KeyVault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="8cda9-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="8cda9-147">Этот командлет возвращает значение только в том случае, если указан параметр *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="8cda9-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="8cda9-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cda9-148">NOTES</span></span>

## <span data-ttu-id="8cda9-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cda9-149">RELATED LINKS</span></span>

[<span data-ttu-id="8cda9-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8cda9-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="8cda9-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8cda9-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="8cda9-152">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="8cda9-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

