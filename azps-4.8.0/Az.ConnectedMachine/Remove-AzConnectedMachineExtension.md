---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079096"
---
# <span data-ttu-id="e618e-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="e618e-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="e618e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e618e-102">SYNOPSIS</span></span>
<span data-ttu-id="e618e-103">Операция удаления расширения.</span><span class="sxs-lookup"><span data-stu-id="e618e-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="e618e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e618e-104">SYNTAX</span></span>

### <span data-ttu-id="e618e-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e618e-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e618e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e618e-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e618e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e618e-107">DESCRIPTION</span></span>
<span data-ttu-id="e618e-108">Операция удаления расширения.</span><span class="sxs-lookup"><span data-stu-id="e618e-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="e618e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e618e-109">EXAMPLES</span></span>

### <span data-ttu-id="e618e-110">Пример 1: удаление расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="e618e-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="e618e-111">Удаляет расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e618e-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="e618e-112">Пример 2: удаление расширения через конвейер</span><span class="sxs-lookup"><span data-stu-id="e618e-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="e618e-113">Удаление всех расширений на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e618e-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="e618e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e618e-114">PARAMETERS</span></span>

### <span data-ttu-id="e618e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e618e-115">-AsJob</span></span>
<span data-ttu-id="e618e-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e618e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e618e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e618e-117">-DefaultProfile</span></span>
<span data-ttu-id="e618e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e618e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e618e-119">-InputObject</span></span>
<span data-ttu-id="e618e-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e618e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e618e-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="e618e-121">-MachineName</span></span>
<span data-ttu-id="e618e-122">Имя компьютера, на котором должно быть удалено расширение.</span><span class="sxs-lookup"><span data-stu-id="e618e-122">The name of the machine where the extension should be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e618e-123">-Name</span></span>
<span data-ttu-id="e618e-124">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="e618e-124">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618e-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="e618e-125">-NoWait</span></span>
<span data-ttu-id="e618e-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="e618e-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e618e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e618e-127">-PassThru</span></span>
<span data-ttu-id="e618e-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e618e-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e618e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e618e-129">-ResourceGroupName</span></span>
<span data-ttu-id="e618e-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e618e-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618e-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e618e-131">-SubscriptionId</span></span>
<span data-ttu-id="e618e-132">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e618e-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e618e-133">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e618e-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e618e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e618e-134">-Confirm</span></span>
<span data-ttu-id="e618e-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e618e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e618e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e618e-136">-WhatIf</span></span>
<span data-ttu-id="e618e-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e618e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e618e-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e618e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e618e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e618e-139">CommonParameters</span></span>
<span data-ttu-id="e618e-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e618e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e618e-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e618e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e618e-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e618e-142">INPUTS</span></span>

### <span data-ttu-id="e618e-143">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="e618e-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="e618e-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e618e-144">OUTPUTS</span></span>

### <span data-ttu-id="e618e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e618e-145">System.Boolean</span></span>

## <span data-ttu-id="e618e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="e618e-146">NOTES</span></span>

<span data-ttu-id="e618e-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e618e-147">ALIASES</span></span>

<span data-ttu-id="e618e-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="e618e-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e618e-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e618e-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e618e-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e618e-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e618e-151">INPUTOBJECT <IConnectedMachineIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e618e-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e618e-152">`[ExtensionName <String>]`: Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="e618e-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="e618e-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e618e-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e618e-154">`[Name <String>]`: Имя гибридного компьютера.</span><span class="sxs-lookup"><span data-stu-id="e618e-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="e618e-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e618e-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e618e-156">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e618e-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e618e-157">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e618e-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e618e-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e618e-158">RELATED LINKS</span></span>

