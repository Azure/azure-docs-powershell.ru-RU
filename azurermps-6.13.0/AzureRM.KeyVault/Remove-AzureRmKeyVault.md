---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: c91bc951ef06f2e591893f0959120cac3700b070
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564399"
---
# <span data-ttu-id="f0a2a-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f0a2a-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="f0a2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a2a-103">Удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0a2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0a2a-104">SYNTAX</span></span>

### <span data-ttu-id="f0a2a-105">ByAvailableVault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0a2a-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0a2a-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="f0a2a-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0a2a-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="f0a2a-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0a2a-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="f0a2a-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0a2a-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="f0a2a-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0a2a-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="f0a2a-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0a2a-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0a2a-111">DESCRIPTION</span></span>
<span data-ttu-id="f0a2a-112">Командлет **Remove-AzureRmKeyVault** удаляет указанное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-112">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="f0a2a-113">Кроме того, она удаляет все ключи и секретные данные, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="f0a2a-114">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="f0a2a-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0a2a-115">EXAMPLES</span></span>

### <span data-ttu-id="f0a2a-116">Пример 1: Удаление хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="f0a2a-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="f0a2a-117">Эта команда удаляет хранилище ключей с именем Contoso03Vault из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="f0a2a-118">Пример 2: Удаление хранилища ключей из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0a2a-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="f0a2a-119">Эта команда удаляет хранилище ключей с именем Contoso03Vault из именованной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="f0a2a-120">Если не указать имя группы ресурсов, командлет выполнит поиск именованного хранилища ключей, которое будет удалено в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="f0a2a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0a2a-121">PARAMETERS</span></span>

### <span data-ttu-id="f0a2a-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0a2a-122">-AsJob</span></span>
<span data-ttu-id="f0a2a-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f0a2a-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0a2a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a2a-124">-DefaultProfile</span></span>
<span data-ttu-id="f0a2a-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f0a2a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0a2a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f0a2a-126">-Force</span></span>
<span data-ttu-id="f0a2a-127">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="f0a2a-128">По умолчанию этот командлет предлагает подтвердить удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="f0a2a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0a2a-129">-InputObject</span></span>
<span data-ttu-id="f0a2a-130">Объект хранилища ключей, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-130">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2a-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f0a2a-131">-InRemovedState</span></span>
<span data-ttu-id="f0a2a-132">Удалить ранее удаленное хранилище без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-132">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2a-133">-Location</span><span class="sxs-lookup"><span data-stu-id="f0a2a-133">-Location</span></span>
<span data-ttu-id="f0a2a-134">Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-134">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2a-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0a2a-135">-PassThru</span></span>
<span data-ttu-id="f0a2a-136">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="f0a2a-137">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-137">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f0a2a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0a2a-138">-ResourceGroupName</span></span>
<span data-ttu-id="f0a2a-139">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-139">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0a2a-140">-ResourceId</span></span>
<span data-ttu-id="f0a2a-141">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-141">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2a-142">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f0a2a-142">-VaultName</span></span>
<span data-ttu-id="f0a2a-143">Указывает имя хранилища ключей, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-143">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0a2a-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0a2a-144">-Confirm</span></span>
<span data-ttu-id="f0a2a-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0a2a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0a2a-146">-WhatIf</span></span>
<span data-ttu-id="f0a2a-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0a2a-148">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0a2a-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0a2a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a2a-150">CommonParameters</span></span>
<span data-ttu-id="f0a2a-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0a2a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a2a-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0a2a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a2a-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0a2a-153">INPUTS</span></span>

### <span data-ttu-id="f0a2a-154">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f0a2a-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="f0a2a-155">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f0a2a-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f0a2a-156">System. String</span><span class="sxs-lookup"><span data-stu-id="f0a2a-156">System.String</span></span>

## <span data-ttu-id="f0a2a-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0a2a-157">OUTPUTS</span></span>

### <span data-ttu-id="f0a2a-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0a2a-158">System.Boolean</span></span>

## <span data-ttu-id="f0a2a-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0a2a-159">NOTES</span></span>

## <span data-ttu-id="f0a2a-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0a2a-160">RELATED LINKS</span></span>

[<span data-ttu-id="f0a2a-161">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f0a2a-161">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="f0a2a-162">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f0a2a-162">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
