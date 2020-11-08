---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/update-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Update-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: a39f347497fe6be31ccb26ce1f726d1eebe155e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243479"
---
# <span data-ttu-id="f5eb6-101">Update-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="f5eb6-101">Update-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="f5eb6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="f5eb6-103">Обновите Теги решения.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-103">Update the tags of a solution.</span></span>

## <span data-ttu-id="f5eb6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5eb6-104">SYNTAX</span></span>

### <span data-ttu-id="f5eb6-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5eb6-105">UpdateExpanded (Default)</span></span>
```
Update-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f5eb6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f5eb6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f5eb6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5eb6-107">DESCRIPTION</span></span>
<span data-ttu-id="f5eb6-108">Обновите Теги решения.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-108">Update the tags of a solution.</span></span>

## <span data-ttu-id="f5eb6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5eb6-109">EXAMPLES</span></span>

### <span data-ttu-id="f5eb6-110">Пример 1: обновление решения для анализа журнала на мониторе по имени</span><span class="sxs-lookup"><span data-stu-id="f5eb6-110">Example 1: Update a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Update-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)' -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="f5eb6-111">Эта команда обновляет решение для анализа журнала на мониторе по имени.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-111">This command updates a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="f5eb6-112">Пример 2: обновление решения для анализа журнала на мониторе по объектам</span><span class="sxs-lookup"><span data-stu-id="f5eb6-112">Example 2: Update a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName lucas-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'
PS C:\> Update-AzMonitorLogAnalyticsSolution -InputObject $monitor -Tag @{'Operation'='update';'Param'='Tag'}

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="f5eb6-113">Эта команда обновляет решение для анализа журнала на мониторе по объектам.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-113">This command updates a monitor log analytics solution by object.</span></span>

## <span data-ttu-id="f5eb6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5eb6-114">PARAMETERS</span></span>

### <span data-ttu-id="f5eb6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5eb6-115">-DefaultProfile</span></span>
<span data-ttu-id="f5eb6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5eb6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5eb6-117">-InputObject</span></span>
<span data-ttu-id="f5eb6-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f5eb6-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5eb6-119">-Name</span></span>
<span data-ttu-id="f5eb6-120">Имя пользовательского решения.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-120">User Solution Name.</span></span>

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

### <span data-ttu-id="f5eb6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5eb6-121">-ResourceGroupName</span></span>
<span data-ttu-id="f5eb6-122">Имя получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-122">The name of the resource group to get.</span></span>
<span data-ttu-id="f5eb6-123">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f5eb6-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5eb6-124">-SubscriptionId</span></span>
<span data-ttu-id="f5eb6-125">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-125">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f5eb6-126">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f5eb6-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="f5eb6-127">-Tag</span></span>
<span data-ttu-id="f5eb6-128">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="f5eb6-128">Resource tags</span></span>

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

### <span data-ttu-id="f5eb6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5eb6-129">-Confirm</span></span>
<span data-ttu-id="f5eb6-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5eb6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5eb6-131">-WhatIf</span></span>
<span data-ttu-id="f5eb6-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5eb6-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5eb6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5eb6-134">CommonParameters</span></span>
<span data-ttu-id="f5eb6-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5eb6-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5eb6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5eb6-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5eb6-137">INPUTS</span></span>

### <span data-ttu-id="f5eb6-138">Microsoft. Azure. PowerShell. командлеты. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="f5eb6-138">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="f5eb6-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5eb6-139">OUTPUTS</span></span>

### <span data-ttu-id="f5eb6-140">Microsoft. Azure. PowerShell. командлеты. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="f5eb6-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="f5eb6-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5eb6-141">NOTES</span></span>

<span data-ttu-id="f5eb6-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="f5eb6-142">ALIASES</span></span>

<span data-ttu-id="f5eb6-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f5eb6-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f5eb6-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5eb6-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f5eb6-146">INPUTOBJECT <IMonitoringSolutionsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="f5eb6-146">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5eb6-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="f5eb6-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5eb6-148">`[ManagementAssociationName <String>]`: Имя пользователя в ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-148">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="f5eb6-149">`[ManagementConfigurationName <String>]`: Имя конфигурации для управления пользователями.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-149">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="f5eb6-150">`[ProviderName <String>]`: Имя поставщика родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-150">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="f5eb6-151">`[ResourceGroupName <String>]`: Имя получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-151">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="f5eb6-152">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="f5eb6-153">`[ResourceName <String>]`: Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-153">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="f5eb6-154">`[ResourceType <String>]`: Тип ресурса для родительского ресурса</span><span class="sxs-lookup"><span data-stu-id="f5eb6-154">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="f5eb6-155">`[SolutionName <String>]`: Имя пользовательского решения.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-155">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="f5eb6-156">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f5eb6-157">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="f5eb6-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f5eb6-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5eb6-158">RELATED LINKS</span></span>

