---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: 777c02f6588d7c1fdb1a1d6e9e9c004f51694293
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012371"
---
# <span data-ttu-id="4fdc0-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="4fdc0-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="4fdc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fdc0-102">SYNOPSIS</span></span>
<span data-ttu-id="4fdc0-103">Операция удаления расширения.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="4fdc0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4fdc0-104">SYNTAX</span></span>

### <span data-ttu-id="4fdc0-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4fdc0-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4fdc0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4fdc0-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4fdc0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fdc0-107">DESCRIPTION</span></span>
<span data-ttu-id="4fdc0-108">Операция удаления расширения.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="4fdc0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4fdc0-109">EXAMPLES</span></span>

### <span data-ttu-id="4fdc0-110">Пример 1. Удаление расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="4fdc0-111">Удаляет расширение на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="4fdc0-112">Пример 2. Удаление расширения через конвейер</span><span class="sxs-lookup"><span data-stu-id="4fdc0-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="4fdc0-113">Удаляет все расширения на указанном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="4fdc0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fdc0-114">PARAMETERS</span></span>

### <span data-ttu-id="4fdc0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fdc0-115">-AsJob</span></span>
<span data-ttu-id="4fdc0-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4fdc0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4fdc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fdc0-117">-DefaultProfile</span></span>
<span data-ttu-id="4fdc0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fdc0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fdc0-119">-InputObject</span></span>
<span data-ttu-id="4fdc0-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4fdc0-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="4fdc0-121">-MachineName</span></span>
<span data-ttu-id="4fdc0-122">Имя компьютера, на котором нужно удалить расширение.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="4fdc0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4fdc0-123">-Name</span></span>
<span data-ttu-id="4fdc0-124">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="4fdc0-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4fdc0-125">-NoWait</span></span>
<span data-ttu-id="4fdc0-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="4fdc0-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4fdc0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fdc0-127">-PassThru</span></span>
<span data-ttu-id="4fdc0-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4fdc0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fdc0-129">-ResourceGroupName</span></span>
<span data-ttu-id="4fdc0-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="4fdc0-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4fdc0-131">-SubscriptionId</span></span>
<span data-ttu-id="4fdc0-132">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4fdc0-133">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4fdc0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fdc0-134">-Confirm</span></span>
<span data-ttu-id="4fdc0-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fdc0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fdc0-136">-WhatIf</span></span>
<span data-ttu-id="4fdc0-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fdc0-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fdc0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fdc0-139">CommonParameters</span></span>
<span data-ttu-id="4fdc0-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fdc0-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fdc0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fdc0-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fdc0-142">INPUTS</span></span>

### <span data-ttu-id="4fdc0-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.IConnectedMa modelseIdentity</span><span class="sxs-lookup"><span data-stu-id="4fdc0-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="4fdc0-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4fdc0-144">OUTPUTS</span></span>

### <span data-ttu-id="4fdc0-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4fdc0-145">System.Boolean</span></span>

## <span data-ttu-id="4fdc0-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4fdc0-146">NOTES</span></span>

<span data-ttu-id="4fdc0-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4fdc0-147">ALIASES</span></span>

<span data-ttu-id="4fdc0-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4fdc0-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4fdc0-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4fdc0-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4fdc0-151">INPUTOBJECT <IConnectedMachineIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="4fdc0-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4fdc0-152">`[ExtensionName <String>]`: имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="4fdc0-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="4fdc0-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4fdc0-154">`[Name <String>]`: имя гибридной машины.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="4fdc0-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4fdc0-156">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4fdc0-157">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="4fdc0-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4fdc0-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fdc0-158">RELATED LINKS</span></span>

