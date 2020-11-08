---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248735"
---
# <span data-ttu-id="f686b-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="f686b-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="f686b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f686b-102">SYNOPSIS</span></span>
<span data-ttu-id="f686b-103">Операция удаления расширения.</span><span class="sxs-lookup"><span data-stu-id="f686b-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="f686b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f686b-104">SYNTAX</span></span>

### <span data-ttu-id="f686b-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f686b-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f686b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f686b-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f686b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f686b-107">DESCRIPTION</span></span>
<span data-ttu-id="f686b-108">Операция удаления расширения.</span><span class="sxs-lookup"><span data-stu-id="f686b-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="f686b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f686b-109">EXAMPLES</span></span>

### <span data-ttu-id="f686b-110">Пример 1: удаление расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="f686b-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="f686b-111">Удаляет расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f686b-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="f686b-112">Пример 2: удаление расширения через конвейер</span><span class="sxs-lookup"><span data-stu-id="f686b-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="f686b-113">Удаление всех расширений на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="f686b-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="f686b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f686b-114">PARAMETERS</span></span>

### <span data-ttu-id="f686b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f686b-115">-AsJob</span></span>
<span data-ttu-id="f686b-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f686b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f686b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f686b-117">-DefaultProfile</span></span>
<span data-ttu-id="f686b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f686b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f686b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f686b-119">-InputObject</span></span>
<span data-ttu-id="f686b-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="f686b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f686b-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="f686b-121">-MachineName</span></span>
<span data-ttu-id="f686b-122">Имя компьютера, на котором должно быть удалено расширение.</span><span class="sxs-lookup"><span data-stu-id="f686b-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="f686b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f686b-123">-Name</span></span>
<span data-ttu-id="f686b-124">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="f686b-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="f686b-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="f686b-125">-NoWait</span></span>
<span data-ttu-id="f686b-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="f686b-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f686b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f686b-127">-PassThru</span></span>
<span data-ttu-id="f686b-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f686b-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f686b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f686b-129">-ResourceGroupName</span></span>
<span data-ttu-id="f686b-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f686b-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="f686b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f686b-131">-SubscriptionId</span></span>
<span data-ttu-id="f686b-132">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f686b-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f686b-133">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="f686b-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f686b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f686b-134">-Confirm</span></span>
<span data-ttu-id="f686b-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f686b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f686b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f686b-136">-WhatIf</span></span>
<span data-ttu-id="f686b-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f686b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f686b-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f686b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f686b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f686b-139">CommonParameters</span></span>
<span data-ttu-id="f686b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f686b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f686b-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f686b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f686b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f686b-142">INPUTS</span></span>

### <span data-ttu-id="f686b-143">Microsoft. Azure. PowerShell. командлеты. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="f686b-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="f686b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f686b-144">OUTPUTS</span></span>

### <span data-ttu-id="f686b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f686b-145">System.Boolean</span></span>

## <span data-ttu-id="f686b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="f686b-146">NOTES</span></span>

<span data-ttu-id="f686b-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="f686b-147">ALIASES</span></span>

<span data-ttu-id="f686b-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f686b-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f686b-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f686b-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f686b-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f686b-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f686b-151">INPUTOBJECT <IConnectedMachineIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="f686b-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f686b-152">`[ExtensionName <String>]`: Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="f686b-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="f686b-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="f686b-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f686b-154">`[Name <String>]`: Имя гибридного компьютера.</span><span class="sxs-lookup"><span data-stu-id="f686b-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="f686b-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f686b-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f686b-156">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f686b-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f686b-157">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="f686b-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f686b-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f686b-158">RELATED LINKS</span></span>

