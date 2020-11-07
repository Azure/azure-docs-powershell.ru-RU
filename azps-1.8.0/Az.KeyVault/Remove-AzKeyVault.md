---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 8332f4a5b14668a767ddf77e974a25a14ac884ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900173"
---
# <span data-ttu-id="d03c3-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d03c3-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="d03c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d03c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d03c3-103">Удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="d03c3-103">Deletes a key vault.</span></span>

## <span data-ttu-id="d03c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d03c3-104">SYNTAX</span></span>

### <span data-ttu-id="d03c3-105">ByAvailableVault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d03c3-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03c3-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="d03c3-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03c3-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="d03c3-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03c3-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="d03c3-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03c3-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="d03c3-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d03c3-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="d03c3-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d03c3-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d03c3-111">DESCRIPTION</span></span>
<span data-ttu-id="d03c3-112">Командлет **Remove-AzKeyVault** удаляет указанное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="d03c3-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="d03c3-113">Кроме того, она удаляет все ключи и секретные данные, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="d03c3-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="d03c3-114">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="d03c3-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="d03c3-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d03c3-115">EXAMPLES</span></span>

### <span data-ttu-id="d03c3-116">Пример 1: Удаление хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="d03c3-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="d03c3-117">Эта команда удаляет хранилище ключей с именем Contoso03Vault из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="d03c3-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="d03c3-118">Пример 2: Удаление хранилища ключей из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d03c3-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="d03c3-119">Эта команда удаляет хранилище ключей с именем Contoso03Vault из именованной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d03c3-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="d03c3-120">Если не указать имя группы ресурсов, командлет выполнит поиск именованного хранилища ключей, которое будет удалено в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="d03c3-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="d03c3-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d03c3-121">PARAMETERS</span></span>

### <span data-ttu-id="d03c3-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d03c3-122">-AsJob</span></span>
<span data-ttu-id="d03c3-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d03c3-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d03c3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d03c3-124">-DefaultProfile</span></span>
<span data-ttu-id="d03c3-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d03c3-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d03c3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d03c3-126">-Force</span></span>
<span data-ttu-id="d03c3-127">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d03c3-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="d03c3-128">По умолчанию этот командлет предлагает подтвердить удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="d03c3-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="d03c3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d03c3-129">-InputObject</span></span>
<span data-ttu-id="d03c3-130">Объект хранилища ключей, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d03c3-130">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="d03c3-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d03c3-131">-InRemovedState</span></span>
<span data-ttu-id="d03c3-132">Удалить ранее удаленное хранилище без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="d03c3-132">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="d03c3-133">-Location</span><span class="sxs-lookup"><span data-stu-id="d03c3-133">-Location</span></span>
<span data-ttu-id="d03c3-134">Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="d03c3-134">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="d03c3-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d03c3-135">-PassThru</span></span>
<span data-ttu-id="d03c3-136">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d03c3-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="d03c3-137">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="d03c3-137">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d03c3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d03c3-138">-ResourceGroupName</span></span>
<span data-ttu-id="d03c3-139">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d03c3-139">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d03c3-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d03c3-140">-ResourceId</span></span>
<span data-ttu-id="d03c3-141">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d03c3-141">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="d03c3-142">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d03c3-142">-VaultName</span></span>
<span data-ttu-id="d03c3-143">Указывает имя хранилища ключей, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d03c3-143">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="d03c3-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d03c3-144">-Confirm</span></span>
<span data-ttu-id="d03c3-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d03c3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d03c3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d03c3-146">-WhatIf</span></span>
<span data-ttu-id="d03c3-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d03c3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d03c3-148">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d03c3-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d03c3-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d03c3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d03c3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d03c3-150">CommonParameters</span></span>
<span data-ttu-id="d03c3-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d03c3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d03c3-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d03c3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d03c3-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d03c3-153">INPUTS</span></span>

### <span data-ttu-id="d03c3-154">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d03c3-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d03c3-155">System. String</span><span class="sxs-lookup"><span data-stu-id="d03c3-155">System.String</span></span>

## <span data-ttu-id="d03c3-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d03c3-156">OUTPUTS</span></span>

### <span data-ttu-id="d03c3-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d03c3-157">System.Boolean</span></span>

## <span data-ttu-id="d03c3-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="d03c3-158">NOTES</span></span>

## <span data-ttu-id="d03c3-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d03c3-159">RELATED LINKS</span></span>

[<span data-ttu-id="d03c3-160">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d03c3-160">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="d03c3-161">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d03c3-161">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
