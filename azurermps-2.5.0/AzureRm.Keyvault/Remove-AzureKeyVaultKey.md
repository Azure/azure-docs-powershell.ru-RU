---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 911ea06fdfa9d4d90f8c9935e3e98c026c70cce5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913337"
---
# <span data-ttu-id="99daf-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="99daf-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="99daf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99daf-102">SYNOPSIS</span></span>
<span data-ttu-id="99daf-103">Удаление ключа из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="99daf-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99daf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99daf-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99daf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99daf-105">DESCRIPTION</span></span>
<span data-ttu-id="99daf-106">Командлет Remove-AzureKeyVaultKey удаляет раздел из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="99daf-106">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="99daf-107">Если клавиша была случайно удалена, ключ может быть восстановлен с помощью Undo-AzureKeyVaultKeyRemoval пользователем, у которого есть особые разрешения на восстановление.</span><span class="sxs-lookup"><span data-stu-id="99daf-107">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="99daf-108">Этот командлет имеет значение High для свойства **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="99daf-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="99daf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99daf-109">EXAMPLES</span></span>

### <span data-ttu-id="99daf-110">Пример 1: Удаление ключа из хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="99daf-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="99daf-111">Эта команда удаляет ключ с именем ITSoftware из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="99daf-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="99daf-112">Пример 2: Удаление ключа без подтверждения пользователя</span><span class="sxs-lookup"><span data-stu-id="99daf-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="99daf-113">Эта команда удаляет ключ с именем ITSoftware из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="99daf-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="99daf-114">Команда определяет параметры *Force* и *Confirm* , поэтому командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="99daf-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="99daf-115">Пример 3: Удаление удаленного ключа из хранилища ключей без возможности восстановления</span><span class="sxs-lookup"><span data-stu-id="99daf-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="99daf-116">Эта команда удаляет ключ с именем ITSoftware из хранилища ключей Contoso без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="99daf-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="99daf-117">Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="99daf-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="99daf-118">Пример 4: Удаление ключей с помощью оператора Pipeline</span><span class="sxs-lookup"><span data-stu-id="99daf-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="99daf-119">Эта команда получает все ключи из хранилища ключей Contoso и передает их в командлет **Where-Object** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="99daf-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="99daf-120">Этот командлет передает ключи со значением $False для атрибута **Enabled** для текущего командлета.</span><span class="sxs-lookup"><span data-stu-id="99daf-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="99daf-121">Этот командлет удаляет эти ключи.</span><span class="sxs-lookup"><span data-stu-id="99daf-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="99daf-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99daf-122">PARAMETERS</span></span>

### <span data-ttu-id="99daf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99daf-123">-DefaultProfile</span></span>
<span data-ttu-id="99daf-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="99daf-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99daf-125">-Force</span><span class="sxs-lookup"><span data-stu-id="99daf-125">-Force</span></span>
<span data-ttu-id="99daf-126">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="99daf-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99daf-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="99daf-127">-InRemovedState</span></span>
<span data-ttu-id="99daf-128">Удаление ранее удаленного ключа без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="99daf-128">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="99daf-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99daf-129">-Name</span></span>
<span data-ttu-id="99daf-130">Задает имя удаляемого ключа.</span><span class="sxs-lookup"><span data-stu-id="99daf-130">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="99daf-131">Этот командлет создает полное доменное имя (FQDN) ключа на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="99daf-131">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99daf-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99daf-132">-PassThru</span></span>
<span data-ttu-id="99daf-133">Указывает на то, что этот командлет возвращает объект **Microsoft. Azure. Commands. KeyVault. Models. KeyBundle** .</span><span class="sxs-lookup"><span data-stu-id="99daf-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="99daf-134">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="99daf-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99daf-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="99daf-135">-VaultName</span></span>
<span data-ttu-id="99daf-136">Указывает имя хранилища ключей, из которого нужно удалить ключ.</span><span class="sxs-lookup"><span data-stu-id="99daf-136">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="99daf-137">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="99daf-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="99daf-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99daf-138">-Confirm</span></span>
<span data-ttu-id="99daf-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="99daf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99daf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99daf-140">-WhatIf</span></span>
<span data-ttu-id="99daf-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="99daf-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99daf-142">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="99daf-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99daf-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="99daf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99daf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99daf-144">CommonParameters</span></span>
<span data-ttu-id="99daf-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99daf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99daf-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99daf-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99daf-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99daf-147">INPUTS</span></span>

### <span data-ttu-id="99daf-148">Подстрок</span><span class="sxs-lookup"><span data-stu-id="99daf-148">String</span></span>

## <span data-ttu-id="99daf-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99daf-149">OUTPUTS</span></span>

### <span data-ttu-id="99daf-150">Microsoft. Azure. Commands. KeyVault. Models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="99daf-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="99daf-151">Этот командлет возвращает значение только в том случае, если указан параметр *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="99daf-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="99daf-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="99daf-152">NOTES</span></span>

## <span data-ttu-id="99daf-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99daf-153">RELATED LINKS</span></span>

[<span data-ttu-id="99daf-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="99daf-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="99daf-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="99daf-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="99daf-156">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="99daf-156">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="99daf-157">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="99daf-157">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

