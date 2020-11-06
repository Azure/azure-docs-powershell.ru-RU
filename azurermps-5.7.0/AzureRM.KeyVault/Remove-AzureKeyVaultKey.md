---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: 5244ed9a8803be07a46c50a15553a4863f7907d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563476"
---
# <span data-ttu-id="599dd-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="599dd-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="599dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="599dd-102">SYNOPSIS</span></span>
<span data-ttu-id="599dd-103">Удаление ключа из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="599dd-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="599dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="599dd-104">SYNTAX</span></span>

### <span data-ttu-id="599dd-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="599dd-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599dd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="599dd-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="599dd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="599dd-107">DESCRIPTION</span></span>
<span data-ttu-id="599dd-108">Командлет Remove-AzureKeyVaultKey удаляет раздел из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="599dd-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="599dd-109">Если клавиша была случайно удалена, ключ может быть восстановлен с помощью Undo-AzureKeyVaultKeyRemoval пользователем, у которого есть особые разрешения на восстановление.</span><span class="sxs-lookup"><span data-stu-id="599dd-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="599dd-110">Этот командлет имеет значение High для свойства **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="599dd-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="599dd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="599dd-111">EXAMPLES</span></span>

### <span data-ttu-id="599dd-112">Пример 1: Удаление ключа из хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="599dd-112">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="599dd-113">Эта команда удаляет ключ с именем ITSoftware из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="599dd-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="599dd-114">Пример 2: Удаление ключа без подтверждения пользователя</span><span class="sxs-lookup"><span data-stu-id="599dd-114">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="599dd-115">Эта команда удаляет ключ с именем ITSoftware из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="599dd-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="599dd-116">Команда определяет параметры *Force* и *Confirm* , поэтому командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="599dd-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="599dd-117">Пример 3: Удаление удаленного ключа из хранилища ключей без возможности восстановления</span><span class="sxs-lookup"><span data-stu-id="599dd-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="599dd-118">Эта команда удаляет ключ с именем ITSoftware из хранилища ключей Contoso без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="599dd-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="599dd-119">Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="599dd-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="599dd-120">Пример 4: Удаление ключей с помощью оператора Pipeline</span><span class="sxs-lookup"><span data-stu-id="599dd-120">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="599dd-121">Эта команда получает все ключи из хранилища ключей Contoso и передает их в командлет **Where-Object** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="599dd-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="599dd-122">Этот командлет передает ключи со значением $False для атрибута **Enabled** для текущего командлета.</span><span class="sxs-lookup"><span data-stu-id="599dd-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="599dd-123">Этот командлет удаляет эти ключи.</span><span class="sxs-lookup"><span data-stu-id="599dd-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="599dd-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="599dd-124">PARAMETERS</span></span>

### <span data-ttu-id="599dd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="599dd-125">-DefaultProfile</span></span>
<span data-ttu-id="599dd-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="599dd-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="599dd-127">-Force</span><span class="sxs-lookup"><span data-stu-id="599dd-127">-Force</span></span>
<span data-ttu-id="599dd-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="599dd-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="599dd-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="599dd-129">-InputObject</span></span>
<span data-ttu-id="599dd-130">Объект KeyBundle</span><span class="sxs-lookup"><span data-stu-id="599dd-130">KeyBundle Object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="599dd-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="599dd-131">-InRemovedState</span></span>
<span data-ttu-id="599dd-132">Удаление ранее удаленного ключа без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="599dd-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="599dd-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="599dd-133">-Name</span></span>
<span data-ttu-id="599dd-134">Задает имя удаляемого ключа.</span><span class="sxs-lookup"><span data-stu-id="599dd-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="599dd-135">Этот командлет создает полное доменное имя (FQDN) ключа на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="599dd-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="599dd-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="599dd-136">-PassThru</span></span>
<span data-ttu-id="599dd-137">Указывает на то, что этот командлет возвращает объект **Microsoft. Azure. Commands. KeyVault. Models. KeyBundle** .</span><span class="sxs-lookup"><span data-stu-id="599dd-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="599dd-138">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="599dd-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="599dd-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="599dd-139">-VaultName</span></span>
<span data-ttu-id="599dd-140">Указывает имя хранилища ключей, из которого нужно удалить ключ.</span><span class="sxs-lookup"><span data-stu-id="599dd-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="599dd-141">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="599dd-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="599dd-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="599dd-142">-Confirm</span></span>
<span data-ttu-id="599dd-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="599dd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="599dd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="599dd-144">-WhatIf</span></span>
<span data-ttu-id="599dd-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="599dd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="599dd-146">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="599dd-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="599dd-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="599dd-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="599dd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="599dd-148">CommonParameters</span></span>
<span data-ttu-id="599dd-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="599dd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="599dd-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="599dd-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="599dd-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="599dd-151">INPUTS</span></span>

### <span data-ttu-id="599dd-152">Подстрок</span><span class="sxs-lookup"><span data-stu-id="599dd-152">String</span></span>

## <span data-ttu-id="599dd-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="599dd-153">OUTPUTS</span></span>

### <span data-ttu-id="599dd-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="599dd-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>
<span data-ttu-id="599dd-155">Этот командлет возвращает значение только в том случае, если указан параметр *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="599dd-155">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="599dd-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="599dd-156">NOTES</span></span>

## <span data-ttu-id="599dd-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="599dd-157">RELATED LINKS</span></span>

[<span data-ttu-id="599dd-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="599dd-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="599dd-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="599dd-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="599dd-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="599dd-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="599dd-161">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="599dd-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

