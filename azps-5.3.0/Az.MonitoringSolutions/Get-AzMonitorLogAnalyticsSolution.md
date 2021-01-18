---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506566"
---
# <span data-ttu-id="bfa5c-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="bfa5c-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="bfa5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfa5c-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa5c-103">Извлекает пользовательское решение.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="bfa5c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bfa5c-104">SYNTAX</span></span>

### <span data-ttu-id="bfa5c-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bfa5c-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfa5c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="bfa5c-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bfa5c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bfa5c-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfa5c-108">Список</span><span class="sxs-lookup"><span data-stu-id="bfa5c-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bfa5c-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfa5c-109">DESCRIPTION</span></span>
<span data-ttu-id="bfa5c-110">Извлекает пользовательское решение.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="bfa5c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bfa5c-111">EXAMPLES</span></span>

### <span data-ttu-id="bfa5c-112">Пример 1. Получить решение для аналитики журналов с отслеживанием по имени</span><span class="sxs-lookup"><span data-stu-id="bfa5c-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="bfa5c-113">Эта команда получает решение для анализа журналов по имени.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="bfa5c-114">Пример 2. Получите решение для аналитики журналов с отслеживанием по ИД ресурсов</span><span class="sxs-lookup"><span data-stu-id="bfa5c-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="bfa5c-115">Эта команда получает решение для анализа журналов журналов по ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="bfa5c-116">Пример 3. Получите решение для анализа журнала журнала с помощью объектов</span><span class="sxs-lookup"><span data-stu-id="bfa5c-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="bfa5c-117">Эта команда получает решение для анализа журнала журнала за объектом.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="bfa5c-118">Пример 4. Получите все решения для анализа журналов в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="bfa5c-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="bfa5c-119">Эта команда получает все решения для анализа журналов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="bfa5c-120">Пример 5. Получите все решения для анализа журналов в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="bfa5c-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="bfa5c-121">Эта команда получает все решения для анализа журналов, в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="bfa5c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfa5c-122">PARAMETERS</span></span>

### <span data-ttu-id="bfa5c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa5c-123">-DefaultProfile</span></span>
<span data-ttu-id="bfa5c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfa5c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfa5c-125">-InputObject</span></span>
<span data-ttu-id="bfa5c-126">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa5c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="bfa5c-127">-Name</span></span>
<span data-ttu-id="bfa5c-128">Имя решения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-128">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa5c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa5c-129">-ResourceGroupName</span></span>
<span data-ttu-id="bfa5c-130">Имя группы ресурсов, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-130">The name of the resource group to get.</span></span>
<span data-ttu-id="bfa5c-131">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa5c-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bfa5c-132">-SubscriptionId</span></span>
<span data-ttu-id="bfa5c-133">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bfa5c-134">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa5c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa5c-135">CommonParameters</span></span>
<span data-ttu-id="bfa5c-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa5c-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfa5c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa5c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfa5c-138">INPUTS</span></span>

### <span data-ttu-id="bfa5c-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="bfa5c-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="bfa5c-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bfa5c-140">OUTPUTS</span></span>

### <span data-ttu-id="bfa5c-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="bfa5c-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="bfa5c-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bfa5c-142">NOTES</span></span>

<span data-ttu-id="bfa5c-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bfa5c-143">ALIASES</span></span>

<span data-ttu-id="bfa5c-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="bfa5c-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bfa5c-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bfa5c-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bfa5c-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="bfa5c-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bfa5c-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="bfa5c-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bfa5c-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="bfa5c-150">`[ManagementConfigurationName <String>]`: Имя конфигурации управления пользователями.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="bfa5c-151">`[ProviderName <String>]`: Имя поставщика родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="bfa5c-152">`[ResourceGroupName <String>]`: имя группы ресурсов, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="bfa5c-153">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="bfa5c-154">`[ResourceName <String>]`: Родительское имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="bfa5c-155">`[ResourceType <String>]`: тип ресурса родительского ресурса</span><span class="sxs-lookup"><span data-stu-id="bfa5c-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="bfa5c-156">`[SolutionName <String>]`: Имя решения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="bfa5c-157">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bfa5c-158">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="bfa5c-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bfa5c-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfa5c-159">RELATED LINKS</span></span>

