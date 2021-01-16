---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406463"
---
# <span data-ttu-id="b209d-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="b209d-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="b209d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b209d-102">SYNOPSIS</span></span>
<span data-ttu-id="b209d-103">Обновив теги решения.</span><span class="sxs-lookup"><span data-stu-id="b209d-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="b209d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b209d-104">SYNTAX</span></span>

### <span data-ttu-id="b209d-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b209d-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b209d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b209d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b209d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b209d-107">DESCRIPTION</span></span>
<span data-ttu-id="b209d-108">Обновив теги решения.</span><span class="sxs-lookup"><span data-stu-id="b209d-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="b209d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b209d-109">EXAMPLES</span></span>

### <span data-ttu-id="b209d-110">Пример 1. Обновление решения для аналитики журналов с именами</span><span class="sxs-lookup"><span data-stu-id="b209d-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="b209d-111">Эта команда обновляет решение для анализа журналов по имени.</span><span class="sxs-lookup"><span data-stu-id="b209d-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="b209d-112">Пример 2. Обновление решения для аналитики журнала журнала с помощью объектов</span><span class="sxs-lookup"><span data-stu-id="b209d-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="b209d-113">Эта команда обновляет решение для анализа журнала журнала за объектом.</span><span class="sxs-lookup"><span data-stu-id="b209d-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="b209d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b209d-114">PARAMETERS</span></span>

### <span data-ttu-id="b209d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b209d-115">-DefaultProfile</span></span>
<span data-ttu-id="b209d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b209d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b209d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b209d-117">-InputObject</span></span>
<span data-ttu-id="b209d-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b209d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b209d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b209d-119">-Name</span></span>
<span data-ttu-id="b209d-120">Имя решения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b209d-120">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b209d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b209d-121">-ResourceGroupName</span></span>
<span data-ttu-id="b209d-122">Имя группы ресурсов, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="b209d-122">The name of the resource group to get.</span></span>
<span data-ttu-id="b209d-123">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b209d-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b209d-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b209d-124">-SubscriptionId</span></span>
<span data-ttu-id="b209d-125">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b209d-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b209d-126">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b209d-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b209d-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b209d-127">-Tag</span></span>
<span data-ttu-id="b209d-128">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="b209d-128">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b209d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b209d-129">-Confirm</span></span>
<span data-ttu-id="b209d-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b209d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b209d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b209d-131">-WhatIf</span></span>
<span data-ttu-id="b209d-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b209d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b209d-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b209d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b209d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b209d-134">CommonParameters</span></span>
<span data-ttu-id="b209d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b209d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b209d-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b209d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b209d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b209d-137">INPUTS</span></span>

### <span data-ttu-id="b209d-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="b209d-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="b209d-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b209d-139">OUTPUTS</span></span>

### <span data-ttu-id="b209d-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="b209d-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="b209d-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b209d-141">NOTES</span></span>

<span data-ttu-id="b209d-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b209d-142">ALIASES</span></span>

<span data-ttu-id="b209d-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b209d-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b209d-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b209d-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b209d-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b209d-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b209d-146">INPUTOBJECT <IMonitoringSolutionsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b209d-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b209d-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b209d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b209d-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="b209d-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="b209d-149">`[ManagementConfigurationName <String>]`: Имя конфигурации управления пользователями.</span><span class="sxs-lookup"><span data-stu-id="b209d-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="b209d-150">`[ProviderName <String>]`: Имя поставщика родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="b209d-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="b209d-151">`[ResourceGroupName <String>]`: имя группы ресурсов, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="b209d-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="b209d-152">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b209d-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="b209d-153">`[ResourceName <String>]`: Родительское имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b209d-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="b209d-154">`[ResourceType <String>]`: тип ресурса родительского ресурса</span><span class="sxs-lookup"><span data-stu-id="b209d-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="b209d-155">`[SolutionName <String>]`: Имя решения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b209d-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="b209d-156">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b209d-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b209d-157">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b209d-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b209d-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b209d-158">RELATED LINKS</span></span>

