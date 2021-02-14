---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243981"
---
# <span data-ttu-id="a67cf-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="a67cf-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="a67cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a67cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a67cf-103">Операция удаления гибридного удостоверения компьютера в Azure.</span><span class="sxs-lookup"><span data-stu-id="a67cf-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="a67cf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a67cf-104">SYNTAX</span></span>

### <span data-ttu-id="a67cf-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a67cf-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a67cf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a67cf-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a67cf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a67cf-107">DESCRIPTION</span></span>
<span data-ttu-id="a67cf-108">Операция удаления гибридного удостоверения компьютера в Azure.</span><span class="sxs-lookup"><span data-stu-id="a67cf-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="a67cf-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a67cf-109">EXAMPLES</span></span>

### <span data-ttu-id="a67cf-110">Пример 1. Удаление подключенного компьютера</span><span class="sxs-lookup"><span data-stu-id="a67cf-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="a67cf-111">Удаляет подключенный компьютер.</span><span class="sxs-lookup"><span data-stu-id="a67cf-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="a67cf-112">Пример 2. Удаление подключенных компьютеров через конвейер</span><span class="sxs-lookup"><span data-stu-id="a67cf-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="a67cf-113">Удаляет все компьютеры в группе `contoso-connected-machines` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a67cf-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="a67cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a67cf-114">PARAMETERS</span></span>

### <span data-ttu-id="a67cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67cf-115">-DefaultProfile</span></span>
<span data-ttu-id="a67cf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a67cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a67cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a67cf-117">-InputObject</span></span>
<span data-ttu-id="a67cf-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a67cf-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a67cf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a67cf-119">-Name</span></span>
<span data-ttu-id="a67cf-120">Имя гибридной машины.</span><span class="sxs-lookup"><span data-stu-id="a67cf-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="a67cf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a67cf-121">-PassThru</span></span>
<span data-ttu-id="a67cf-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="a67cf-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a67cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a67cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="a67cf-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a67cf-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a67cf-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a67cf-125">-SubscriptionId</span></span>
<span data-ttu-id="a67cf-126">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a67cf-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a67cf-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="a67cf-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a67cf-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a67cf-128">-Confirm</span></span>
<span data-ttu-id="a67cf-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a67cf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a67cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a67cf-130">-WhatIf</span></span>
<span data-ttu-id="a67cf-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a67cf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a67cf-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a67cf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a67cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67cf-133">CommonParameters</span></span>
<span data-ttu-id="a67cf-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a67cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67cf-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a67cf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67cf-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a67cf-136">INPUTS</span></span>

### <span data-ttu-id="a67cf-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.IConnectedMa modelseIdentity</span><span class="sxs-lookup"><span data-stu-id="a67cf-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="a67cf-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a67cf-138">OUTPUTS</span></span>

### <span data-ttu-id="a67cf-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a67cf-139">System.Boolean</span></span>

## <span data-ttu-id="a67cf-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a67cf-140">NOTES</span></span>

<span data-ttu-id="a67cf-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a67cf-141">ALIASES</span></span>

<span data-ttu-id="a67cf-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a67cf-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a67cf-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a67cf-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a67cf-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a67cf-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a67cf-145">INPUTOBJECT <IConnectedMachineIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a67cf-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a67cf-146">`[ExtensionName <String>]`: имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="a67cf-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="a67cf-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="a67cf-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a67cf-148">`[Name <String>]`: имя гибридной машины.</span><span class="sxs-lookup"><span data-stu-id="a67cf-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="a67cf-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a67cf-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a67cf-150">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a67cf-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a67cf-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="a67cf-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a67cf-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a67cf-152">RELATED LINKS</span></span>

