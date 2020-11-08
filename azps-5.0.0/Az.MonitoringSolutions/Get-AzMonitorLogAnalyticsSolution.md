---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/get-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Get-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a353269f884e9d8ea4fe87a4f7396f4e886610ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250023"
---
# <span data-ttu-id="d4f1d-101">Get-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="d4f1d-101">Get-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="d4f1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f1d-103">Извлекает решение пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-103">Retrieves the user solution.</span></span>

## <span data-ttu-id="d4f1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4f1d-104">SYNTAX</span></span>

### <span data-ttu-id="d4f1d-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4f1d-105">List1 (Default)</span></span>
```
Get-AzMonitorLogAnalyticsSolution [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4f1d-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d4f1d-106">Get</span></span>
```
Get-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4f1d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d4f1d-107">GetViaIdentity</span></span>
```
Get-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4f1d-108">Список</span><span class="sxs-lookup"><span data-stu-id="d4f1d-108">List</span></span>
```
Get-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d4f1d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4f1d-109">DESCRIPTION</span></span>
<span data-ttu-id="d4f1d-110">Извлекает решение пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-110">Retrieves the user solution.</span></span>

## <span data-ttu-id="d4f1d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4f1d-111">EXAMPLES</span></span>

### <span data-ttu-id="d4f1d-112">Пример 1: получение решения для анализа журнала на мониторе по имени</span><span class="sxs-lookup"><span data-stu-id="d4f1d-112">Example 1: Get a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="d4f1d-113">Эта команда получает решение для анализа журнала на мониторе по имени.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-113">This command gets a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="d4f1d-114">Пример 2: получение решения для анализа журнала на мониторе по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="d4f1d-114">Example 2: Get a monitor log analytics solution by resource id</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/azureps-manual-test/providers/Microsoft.OperationsManagement/solutions/Containers(monitoringworkspace-t01)"} | Get-AzMonitorLogAnalyticsSolution

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="d4f1d-115">Эта команда получает решение для аналитики журнала на мониторе по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-115">This command gets a monitor log analytics solution by resource id.</span></span>

### <span data-ttu-id="d4f1d-116">Пример 3: получение решения для анализа журнала на мониторе по объектам</span><span class="sxs-lookup"><span data-stu-id="d4f1d-116">Example 3: Get a monitor log analytics solution by object</span></span>
```powershell

PS C:\> $monitor = New-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor -Name 'Containers(azureps-monitor)'
PS C:\> Get-AzMonitorLogAnalyticsSolution -InputObject $monitor
Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="d4f1d-117">Эта команда получает решение для анализа журнала на мониторе по объектам.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-117">This command gets a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="d4f1d-118">Пример 4: получение всех решений для анализа журнала на мониторе в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="d4f1d-118">Example 4: Get all monitor log analytics solutions under a resource group</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-monitor

Name                      Type                                     Location
----                      ----                                     --------
Containers(azureps-monitor) Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="d4f1d-119">Эта команда получает все решения для аналитических журналов на мониторе в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-119">This command gets all monitor log analytics solutions under a resource group.</span></span>

### <span data-ttu-id="d4f1d-120">Пример 5: получение всех решений для анализа журнала на мониторе в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="d4f1d-120">Example 5: Get all monitor log analytics solutions under a subscription</span></span>
```powershell
PS C:\> Get-AzMonitorLogAnalyticsSolution 

Name                                Type                                     Location
----                                ----                                     --------
Containers(monitoringworkspace-t01) Microsoft.OperationsManagement/solutions East US
Containers(azureps-monitor)           Microsoft.OperationsManagement/solutions West US 2
```

<span data-ttu-id="d4f1d-121">Эта команда получает все решения для аналитических журналов на мониторе в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-121">This command gets all monitor log analytics solutions under a subscription.</span></span>

## <span data-ttu-id="d4f1d-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4f1d-122">PARAMETERS</span></span>

### <span data-ttu-id="d4f1d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f1d-123">-DefaultProfile</span></span>
<span data-ttu-id="d4f1d-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4f1d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4f1d-125">-InputObject</span></span>
<span data-ttu-id="d4f1d-126">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d4f1d-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d4f1d-127">-Name</span></span>
<span data-ttu-id="d4f1d-128">Имя пользовательского решения.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-128">User Solution Name.</span></span>

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

### <span data-ttu-id="d4f1d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4f1d-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4f1d-130">Имя получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-130">The name of the resource group to get.</span></span>
<span data-ttu-id="d4f1d-131">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d4f1d-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4f1d-132">-SubscriptionId</span></span>
<span data-ttu-id="d4f1d-133">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4f1d-134">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d4f1d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f1d-135">CommonParameters</span></span>
<span data-ttu-id="d4f1d-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f1d-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4f1d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f1d-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4f1d-138">INPUTS</span></span>

### <span data-ttu-id="d4f1d-139">Microsoft. Azure. PowerShell. командлеты. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="d4f1d-139">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="d4f1d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4f1d-140">OUTPUTS</span></span>

### <span data-ttu-id="d4f1d-141">Microsoft. Azure. PowerShell. командлеты. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="d4f1d-141">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="d4f1d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4f1d-142">NOTES</span></span>

<span data-ttu-id="d4f1d-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d4f1d-143">ALIASES</span></span>

<span data-ttu-id="d4f1d-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d4f1d-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4f1d-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4f1d-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4f1d-147">INPUTOBJECT <IMonitoringSolutionsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d4f1d-147">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4f1d-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d4f1d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4f1d-149">`[ManagementAssociationName <String>]`: Имя пользователя в ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-149">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="d4f1d-150">`[ManagementConfigurationName <String>]`: Имя конфигурации для управления пользователями.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-150">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="d4f1d-151">`[ProviderName <String>]`: Имя поставщика родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-151">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="d4f1d-152">`[ResourceGroupName <String>]`: Имя получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-152">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="d4f1d-153">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="d4f1d-154">`[ResourceName <String>]`: Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-154">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="d4f1d-155">`[ResourceType <String>]`: Тип ресурса для родительского ресурса</span><span class="sxs-lookup"><span data-stu-id="d4f1d-155">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="d4f1d-156">`[SolutionName <String>]`: Имя пользовательского решения.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-156">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="d4f1d-157">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-157">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d4f1d-158">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d4f1d-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4f1d-159">RELATED LINKS</span></span>

