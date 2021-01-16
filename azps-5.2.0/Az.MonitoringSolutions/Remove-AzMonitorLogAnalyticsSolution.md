---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400815"
---
# <span data-ttu-id="1898c-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="1898c-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="1898c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1898c-102">SYNOPSIS</span></span>
<span data-ttu-id="1898c-103">Удаляет решение из подписки.</span><span class="sxs-lookup"><span data-stu-id="1898c-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="1898c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1898c-104">SYNTAX</span></span>

### <span data-ttu-id="1898c-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1898c-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1898c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1898c-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1898c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1898c-107">DESCRIPTION</span></span>
<span data-ttu-id="1898c-108">Удаляет решение из подписки.</span><span class="sxs-lookup"><span data-stu-id="1898c-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="1898c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1898c-109">EXAMPLES</span></span>

### <span data-ttu-id="1898c-110">Пример 1. Удаление решения для аналитики журналов с отслеживанием по имени</span><span class="sxs-lookup"><span data-stu-id="1898c-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="1898c-111">Эта команда удаляет по имени решение для анализа журналов.</span><span class="sxs-lookup"><span data-stu-id="1898c-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="1898c-112">Пример 2. Удаление решения для анализа журнала журнала за объектом</span><span class="sxs-lookup"><span data-stu-id="1898c-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="1898c-113">Эта команда удаляет решение для анализа журнала журнала за объектом.</span><span class="sxs-lookup"><span data-stu-id="1898c-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="1898c-114">Пример 3. Удаление решения для аналитики журналов с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="1898c-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="1898c-115">Эта команда удаляет решение для аналитики журналов за счет конвейера.</span><span class="sxs-lookup"><span data-stu-id="1898c-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="1898c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1898c-116">PARAMETERS</span></span>

### <span data-ttu-id="1898c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1898c-117">-DefaultProfile</span></span>
<span data-ttu-id="1898c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1898c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1898c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1898c-119">-InputObject</span></span>
<span data-ttu-id="1898c-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="1898c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1898c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1898c-121">-Name</span></span>
<span data-ttu-id="1898c-122">Имя решения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1898c-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1898c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1898c-123">-PassThru</span></span>
<span data-ttu-id="1898c-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="1898c-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1898c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1898c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1898c-126">Имя группы ресурсов, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="1898c-126">The name of the resource group to get.</span></span>
<span data-ttu-id="1898c-127">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="1898c-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1898c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1898c-128">-SubscriptionId</span></span>
<span data-ttu-id="1898c-129">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1898c-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1898c-130">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1898c-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1898c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1898c-131">-Confirm</span></span>
<span data-ttu-id="1898c-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1898c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1898c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1898c-133">-WhatIf</span></span>
<span data-ttu-id="1898c-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1898c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1898c-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1898c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1898c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1898c-136">CommonParameters</span></span>
<span data-ttu-id="1898c-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1898c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1898c-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1898c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1898c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1898c-139">INPUTS</span></span>

### <span data-ttu-id="1898c-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="1898c-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="1898c-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1898c-141">OUTPUTS</span></span>

### <span data-ttu-id="1898c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1898c-142">System.Boolean</span></span>

## <span data-ttu-id="1898c-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1898c-143">NOTES</span></span>

<span data-ttu-id="1898c-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1898c-144">ALIASES</span></span>

<span data-ttu-id="1898c-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1898c-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1898c-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="1898c-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1898c-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1898c-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1898c-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="1898c-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1898c-149">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="1898c-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1898c-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="1898c-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="1898c-151">`[ManagementConfigurationName <String>]`: Имя конфигурации управления пользователями.</span><span class="sxs-lookup"><span data-stu-id="1898c-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="1898c-152">`[ProviderName <String>]`: Имя поставщика родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="1898c-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="1898c-153">`[ResourceGroupName <String>]`: имя группы ресурсов, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="1898c-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="1898c-154">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="1898c-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="1898c-155">`[ResourceName <String>]`: Родительское имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="1898c-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="1898c-156">`[ResourceType <String>]`: тип ресурса родительского ресурса</span><span class="sxs-lookup"><span data-stu-id="1898c-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="1898c-157">`[SolutionName <String>]`: Имя решения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1898c-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="1898c-158">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1898c-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1898c-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1898c-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1898c-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1898c-160">RELATED LINKS</span></span>

