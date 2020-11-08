---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
ms.openlocfilehash: 6555299726d8dcf443382f72c2aba6324b6b377d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245294"
---
# <span data-ttu-id="48ae3-101">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="48ae3-101">Remove-AzManagedHsm</span></span>

## <span data-ttu-id="48ae3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="48ae3-103">Удаляет управляемый HSM-аппарат.</span><span class="sxs-lookup"><span data-stu-id="48ae3-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="48ae3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48ae3-104">SYNTAX</span></span>

### <span data-ttu-id="48ae3-105">RemoveManagedHsmByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48ae3-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ae3-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="48ae3-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ae3-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="48ae3-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48ae3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48ae3-108">DESCRIPTION</span></span>
<span data-ttu-id="48ae3-109">Командлет **Remove-AzManagedHsm** удаляет указанный управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="48ae3-109">The **Remove-AzManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="48ae3-110">Также удаляются все ключи, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="48ae3-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="48ae3-111">Обратите внимание, что хотя указывать группу ресурсов необязательно для этого командлета, вы должны для лучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="48ae3-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="48ae3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48ae3-112">EXAMPLES</span></span>

### <span data-ttu-id="48ae3-113">Пример 1: Удаление управляемого HSM-кода</span><span class="sxs-lookup"><span data-stu-id="48ae3-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="48ae3-114">Эта команда удаляет управляемый HSM с именем myhsm из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="48ae3-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="48ae3-115">Пример 2: Удаление управляемого HSM-кода из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="48ae3-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="48ae3-116">Эта команда удаляет управляемый HSM, именуемый myhsm, из группы ресурсов с именем myrg1.</span><span class="sxs-lookup"><span data-stu-id="48ae3-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="48ae3-117">Если вы не укажете имя группы ресурсов, командлет выполнит поиск именованного управляемого HSM для удаления в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="48ae3-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="48ae3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48ae3-118">PARAMETERS</span></span>

### <span data-ttu-id="48ae3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48ae3-119">-AsJob</span></span>
<span data-ttu-id="48ae3-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="48ae3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48ae3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ae3-121">-DefaultProfile</span></span>
<span data-ttu-id="48ae3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48ae3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48ae3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="48ae3-123">-Force</span></span>
<span data-ttu-id="48ae3-124">Указывает на то, что командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="48ae3-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="48ae3-125">По умолчанию этот командлет предлагает подтвердить необходимость удаления управляемого HSM.</span><span class="sxs-lookup"><span data-stu-id="48ae3-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="48ae3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48ae3-126">-InputObject</span></span>
<span data-ttu-id="48ae3-127">Управляемый объект HSM, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="48ae3-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48ae3-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="48ae3-128">-Name</span></span>
<span data-ttu-id="48ae3-129">Указывает имя управляемого HSM, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="48ae3-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ae3-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48ae3-130">-PassThru</span></span>
<span data-ttu-id="48ae3-131">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="48ae3-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="48ae3-132">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="48ae3-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="48ae3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ae3-133">-ResourceGroupName</span></span>
<span data-ttu-id="48ae3-134">Указывает имя группы ресурсов для управляемого HSM Azure, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="48ae3-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ae3-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48ae3-135">-ResourceId</span></span>
<span data-ttu-id="48ae3-136">Идентификатор ресурса ManagedHsm.</span><span class="sxs-lookup"><span data-stu-id="48ae3-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48ae3-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48ae3-137">-Confirm</span></span>
<span data-ttu-id="48ae3-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48ae3-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ae3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48ae3-139">-WhatIf</span></span>
<span data-ttu-id="48ae3-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48ae3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48ae3-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48ae3-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ae3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ae3-142">CommonParameters</span></span>
<span data-ttu-id="48ae3-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48ae3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ae3-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48ae3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ae3-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48ae3-145">INPUTS</span></span>

### <span data-ttu-id="48ae3-146">Microsoft. Azure. Commands. KeyVault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="48ae3-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="48ae3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="48ae3-147">System.String</span></span>

## <span data-ttu-id="48ae3-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48ae3-148">OUTPUTS</span></span>

### <span data-ttu-id="48ae3-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48ae3-149">System.Boolean</span></span>

## <span data-ttu-id="48ae3-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="48ae3-150">NOTES</span></span>

## <span data-ttu-id="48ae3-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48ae3-151">RELATED LINKS</span></span>

[<span data-ttu-id="48ae3-152">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="48ae3-152">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="48ae3-153">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="48ae3-153">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="48ae3-154">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="48ae3-154">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)