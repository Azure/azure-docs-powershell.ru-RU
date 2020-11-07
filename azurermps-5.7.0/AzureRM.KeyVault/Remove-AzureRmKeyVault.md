---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 0c9e37433d28a16a28ca56daf4a726347b7a9533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732855"
---
# <span data-ttu-id="58501-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="58501-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="58501-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58501-102">SYNOPSIS</span></span>
<span data-ttu-id="58501-103">Удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="58501-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58501-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58501-104">SYNTAX</span></span>

### <span data-ttu-id="58501-105">ByAvailableVault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58501-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58501-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="58501-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58501-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="58501-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58501-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="58501-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58501-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58501-109">DESCRIPTION</span></span>
<span data-ttu-id="58501-110">Командлет **Remove-AzureRmKeyVault** удаляет указанное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="58501-110">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="58501-111">Кроме того, она удаляет все ключи и секретные данные, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="58501-111">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="58501-112">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="58501-112">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="58501-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58501-113">EXAMPLES</span></span>

### <span data-ttu-id="58501-114">Пример 1: Удаление хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="58501-114">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="58501-115">Эта команда удаляет хранилище ключей с именем Contoso03Vault из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="58501-115">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="58501-116">Пример 2: Удаление хранилища ключей из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="58501-116">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="58501-117">Эта команда удаляет хранилище ключей с именем Contoso03Vault из именованной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58501-117">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="58501-118">Если не указать имя группы ресурсов, командлет выполнит поиск именованного хранилища ключей, которое будет удалено в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="58501-118">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="58501-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58501-119">PARAMETERS</span></span>

### <span data-ttu-id="58501-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58501-120">-AsJob</span></span>
<span data-ttu-id="58501-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="58501-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58501-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58501-122">-DefaultProfile</span></span>
<span data-ttu-id="58501-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="58501-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58501-124">-Force</span><span class="sxs-lookup"><span data-stu-id="58501-124">-Force</span></span>
<span data-ttu-id="58501-125">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="58501-125">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="58501-126">По умолчанию этот командлет предлагает подтвердить удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="58501-126">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="58501-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58501-127">-InputObject</span></span>
<span data-ttu-id="58501-128">Объект хранилища ключей, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="58501-128">Key Vault object to be deleted.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58501-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="58501-129">-InRemovedState</span></span>
<span data-ttu-id="58501-130">Удалить ранее удаленное хранилище без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="58501-130">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58501-131">-Location</span><span class="sxs-lookup"><span data-stu-id="58501-131">-Location</span></span>
<span data-ttu-id="58501-132">Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="58501-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58501-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58501-133">-PassThru</span></span>
<span data-ttu-id="58501-134">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="58501-134">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="58501-135">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="58501-135">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="58501-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58501-136">-ResourceGroupName</span></span>
<span data-ttu-id="58501-137">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58501-137">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58501-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="58501-138">-VaultName</span></span>
<span data-ttu-id="58501-139">Указывает имя хранилища ключей, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="58501-139">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58501-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58501-140">-Confirm</span></span>
<span data-ttu-id="58501-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="58501-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58501-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58501-142">-WhatIf</span></span>
<span data-ttu-id="58501-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58501-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58501-144">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58501-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58501-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="58501-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58501-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58501-146">CommonParameters</span></span>
<span data-ttu-id="58501-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58501-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58501-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58501-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58501-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58501-149">INPUTS</span></span>

### <span data-ttu-id="58501-150">Ничего</span><span class="sxs-lookup"><span data-stu-id="58501-150">None</span></span>
<span data-ttu-id="58501-151">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="58501-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58501-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58501-152">OUTPUTS</span></span>

### <span data-ttu-id="58501-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58501-153">System.Boolean</span></span>

## <span data-ttu-id="58501-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="58501-154">NOTES</span></span>

## <span data-ttu-id="58501-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58501-155">RELATED LINKS</span></span>

[<span data-ttu-id="58501-156">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="58501-156">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="58501-157">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="58501-157">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
