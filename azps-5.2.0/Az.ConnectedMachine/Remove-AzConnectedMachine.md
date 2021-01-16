---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325642"
---
# <span data-ttu-id="47b6b-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="47b6b-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="47b6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="47b6b-103">Операция удаления гибридного удостоверения компьютера в Azure.</span><span class="sxs-lookup"><span data-stu-id="47b6b-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="47b6b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47b6b-104">SYNTAX</span></span>

### <span data-ttu-id="47b6b-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47b6b-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="47b6b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47b6b-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47b6b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47b6b-107">DESCRIPTION</span></span>
<span data-ttu-id="47b6b-108">Операция удаления гибридного удостоверения компьютера в Azure.</span><span class="sxs-lookup"><span data-stu-id="47b6b-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="47b6b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47b6b-109">EXAMPLES</span></span>

### <span data-ttu-id="47b6b-110">Пример 1. Удаление подключенного компьютера</span><span class="sxs-lookup"><span data-stu-id="47b6b-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="47b6b-111">Удаляет подключенный компьютер.</span><span class="sxs-lookup"><span data-stu-id="47b6b-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="47b6b-112">Пример 2. Удаление подключенных компьютеров через конвейер</span><span class="sxs-lookup"><span data-stu-id="47b6b-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="47b6b-113">Удаляет все компьютеры в группе `contoso-connected-machines` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47b6b-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="47b6b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47b6b-114">PARAMETERS</span></span>

### <span data-ttu-id="47b6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b6b-115">-DefaultProfile</span></span>
<span data-ttu-id="47b6b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47b6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b6b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47b6b-117">-InputObject</span></span>
<span data-ttu-id="47b6b-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="47b6b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="47b6b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="47b6b-119">-Name</span></span>
<span data-ttu-id="47b6b-120">Имя гибридной машины.</span><span class="sxs-lookup"><span data-stu-id="47b6b-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="47b6b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47b6b-121">-PassThru</span></span>
<span data-ttu-id="47b6b-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="47b6b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="47b6b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b6b-123">-ResourceGroupName</span></span>
<span data-ttu-id="47b6b-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47b6b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="47b6b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47b6b-125">-SubscriptionId</span></span>
<span data-ttu-id="47b6b-126">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47b6b-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="47b6b-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="47b6b-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="47b6b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47b6b-128">-Confirm</span></span>
<span data-ttu-id="47b6b-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b6b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47b6b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b6b-130">-WhatIf</span></span>
<span data-ttu-id="47b6b-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b6b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b6b-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47b6b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47b6b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b6b-133">CommonParameters</span></span>
<span data-ttu-id="47b6b-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b6b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b6b-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47b6b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b6b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47b6b-136">INPUTS</span></span>

### <span data-ttu-id="47b6b-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.IConnectedMa modelseIdentity</span><span class="sxs-lookup"><span data-stu-id="47b6b-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="47b6b-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47b6b-138">OUTPUTS</span></span>

### <span data-ttu-id="47b6b-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47b6b-139">System.Boolean</span></span>

## <span data-ttu-id="47b6b-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47b6b-140">NOTES</span></span>

<span data-ttu-id="47b6b-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="47b6b-141">ALIASES</span></span>

<span data-ttu-id="47b6b-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="47b6b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47b6b-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="47b6b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47b6b-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47b6b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47b6b-145">INPUTOBJECT <IConnectedMachineIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="47b6b-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47b6b-146">`[ExtensionName <String>]`: имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="47b6b-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="47b6b-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="47b6b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47b6b-148">`[Name <String>]`: имя гибридной машины.</span><span class="sxs-lookup"><span data-stu-id="47b6b-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="47b6b-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47b6b-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="47b6b-150">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47b6b-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="47b6b-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="47b6b-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="47b6b-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47b6b-152">RELATED LINKS</span></span>
