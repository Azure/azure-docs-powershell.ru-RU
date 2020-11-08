---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245302"
---
# <span data-ttu-id="b58cf-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="b58cf-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="b58cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b58cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b58cf-103">Удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b58cf-103">Deletes a key vault.</span></span>

## <span data-ttu-id="b58cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b58cf-104">SYNTAX</span></span>

### <span data-ttu-id="b58cf-105">ByAvailableVault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b58cf-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b58cf-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="b58cf-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b58cf-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="b58cf-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b58cf-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="b58cf-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b58cf-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="b58cf-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b58cf-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="b58cf-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b58cf-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b58cf-111">DESCRIPTION</span></span>
<span data-ttu-id="b58cf-112">Командлет **Remove-AzKeyVault** удаляет указанное хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="b58cf-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="b58cf-113">Кроме того, она удаляет все ключи и секретные данные, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="b58cf-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="b58cf-114">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="b58cf-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="b58cf-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b58cf-115">EXAMPLES</span></span>

### <span data-ttu-id="b58cf-116">Пример 1: Удаление хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="b58cf-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="b58cf-117">Эта команда удаляет хранилище ключей с именем Contoso03Vault из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="b58cf-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="b58cf-118">Пример 2: Удаление хранилища ключей из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b58cf-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="b58cf-119">Эта команда удаляет хранилище ключей с именем Contoso03Vault из именованной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b58cf-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="b58cf-120">Если не указать имя группы ресурсов, командлет выполнит поиск именованного хранилища ключей, которое будет удалено в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b58cf-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="b58cf-121">Пример 3: Удаление управляемого HSM-кода</span><span class="sxs-lookup"><span data-stu-id="b58cf-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="b58cf-122">Эта команда удаляет управляемый HSM с именем testManagedHsm из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="b58cf-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="b58cf-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b58cf-123">PARAMETERS</span></span>

### <span data-ttu-id="b58cf-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b58cf-124">-AsJob</span></span>
<span data-ttu-id="b58cf-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b58cf-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b58cf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b58cf-126">-DefaultProfile</span></span>
<span data-ttu-id="b58cf-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b58cf-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b58cf-128">-Force</span><span class="sxs-lookup"><span data-stu-id="b58cf-128">-Force</span></span>
<span data-ttu-id="b58cf-129">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b58cf-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="b58cf-130">По умолчанию этот командлет предлагает подтвердить удаление хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b58cf-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="b58cf-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b58cf-131">-InputObject</span></span>
<span data-ttu-id="b58cf-132">Объект хранилища ключей, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b58cf-132">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="b58cf-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b58cf-133">-InRemovedState</span></span>
<span data-ttu-id="b58cf-134">Удалить ранее удаленное хранилище без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="b58cf-134">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="b58cf-135">-Location</span><span class="sxs-lookup"><span data-stu-id="b58cf-135">-Location</span></span>
<span data-ttu-id="b58cf-136">Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="b58cf-136">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="b58cf-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b58cf-137">-PassThru</span></span>
<span data-ttu-id="b58cf-138">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b58cf-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="b58cf-139">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="b58cf-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b58cf-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b58cf-140">-ResourceGroupName</span></span>
<span data-ttu-id="b58cf-141">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b58cf-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b58cf-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b58cf-142">-ResourceId</span></span>
<span data-ttu-id="b58cf-143">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="b58cf-143">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="b58cf-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b58cf-144">-VaultName</span></span>
<span data-ttu-id="b58cf-145">Указывает имя хранилища ключей, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b58cf-145">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b58cf-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b58cf-146">-Confirm</span></span>
<span data-ttu-id="b58cf-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b58cf-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b58cf-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b58cf-148">-WhatIf</span></span>
<span data-ttu-id="b58cf-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b58cf-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b58cf-150">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b58cf-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b58cf-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b58cf-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b58cf-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b58cf-152">CommonParameters</span></span>
<span data-ttu-id="b58cf-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b58cf-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b58cf-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b58cf-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b58cf-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b58cf-155">INPUTS</span></span>

### <span data-ttu-id="b58cf-156">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b58cf-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b58cf-157">System. String</span><span class="sxs-lookup"><span data-stu-id="b58cf-157">System.String</span></span>

## <span data-ttu-id="b58cf-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b58cf-158">OUTPUTS</span></span>

### <span data-ttu-id="b58cf-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b58cf-159">System.Boolean</span></span>

## <span data-ttu-id="b58cf-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="b58cf-160">NOTES</span></span>

## <span data-ttu-id="b58cf-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b58cf-161">RELATED LINKS</span></span>

[<span data-ttu-id="b58cf-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="b58cf-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="b58cf-163">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="b58cf-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
