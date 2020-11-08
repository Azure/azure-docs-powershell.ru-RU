---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249401"
---
# <span data-ttu-id="ef645-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="ef645-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="ef645-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef645-102">SYNOPSIS</span></span>
<span data-ttu-id="ef645-103">Удаляет решение в подписке.</span><span class="sxs-lookup"><span data-stu-id="ef645-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="ef645-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef645-104">SYNTAX</span></span>

### <span data-ttu-id="ef645-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ef645-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ef645-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ef645-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef645-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef645-107">DESCRIPTION</span></span>
<span data-ttu-id="ef645-108">Удаляет решение в подписке.</span><span class="sxs-lookup"><span data-stu-id="ef645-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="ef645-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef645-109">EXAMPLES</span></span>

### <span data-ttu-id="ef645-110">Пример 1: Удаление решения для аналитического анализа журналов по имени</span><span class="sxs-lookup"><span data-stu-id="ef645-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="ef645-111">Эта команда удаляет решение "анализ журнала" на мониторе по имени.</span><span class="sxs-lookup"><span data-stu-id="ef645-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="ef645-112">Пример 2: Удаление решения для анализа журнала мониторинга по объектам</span><span class="sxs-lookup"><span data-stu-id="ef645-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="ef645-113">Эта команда удаляет решение "анализ журнала" на мониторе по объектам.</span><span class="sxs-lookup"><span data-stu-id="ef645-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="ef645-114">Пример 3: Удаление решения аналитического анализа журнала на мониторе в канале продаж</span><span class="sxs-lookup"><span data-stu-id="ef645-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="ef645-115">Эта команда удаляет решение для аналитических журналов на мониторе по каналам продаж.</span><span class="sxs-lookup"><span data-stu-id="ef645-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="ef645-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef645-116">PARAMETERS</span></span>

### <span data-ttu-id="ef645-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef645-117">-DefaultProfile</span></span>
<span data-ttu-id="ef645-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef645-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef645-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef645-119">-InputObject</span></span>
<span data-ttu-id="ef645-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ef645-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ef645-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef645-121">-Name</span></span>
<span data-ttu-id="ef645-122">Имя пользовательского решения.</span><span class="sxs-lookup"><span data-stu-id="ef645-122">User Solution Name.</span></span>

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

### <span data-ttu-id="ef645-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef645-123">-PassThru</span></span>
<span data-ttu-id="ef645-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ef645-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ef645-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef645-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef645-126">Имя получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef645-126">The name of the resource group to get.</span></span>
<span data-ttu-id="ef645-127">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="ef645-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ef645-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef645-128">-SubscriptionId</span></span>
<span data-ttu-id="ef645-129">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ef645-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef645-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ef645-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ef645-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef645-131">-Confirm</span></span>
<span data-ttu-id="ef645-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef645-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef645-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef645-133">-WhatIf</span></span>
<span data-ttu-id="ef645-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef645-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef645-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef645-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef645-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef645-136">CommonParameters</span></span>
<span data-ttu-id="ef645-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef645-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef645-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef645-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef645-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef645-139">INPUTS</span></span>

### <span data-ttu-id="ef645-140">Microsoft. Azure. PowerShell. командлеты. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="ef645-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="ef645-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef645-141">OUTPUTS</span></span>

### <span data-ttu-id="ef645-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef645-142">System.Boolean</span></span>

## <span data-ttu-id="ef645-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef645-143">NOTES</span></span>

<span data-ttu-id="ef645-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ef645-144">ALIASES</span></span>

<span data-ttu-id="ef645-145">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ef645-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ef645-146">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ef645-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef645-147">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ef645-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ef645-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="ef645-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef645-149">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="ef645-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef645-150">`[ManagementAssociationName <String>]`: Имя пользователя в ManagementAssociation.</span><span class="sxs-lookup"><span data-stu-id="ef645-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="ef645-151">`[ManagementConfigurationName <String>]`: Имя конфигурации для управления пользователями.</span><span class="sxs-lookup"><span data-stu-id="ef645-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="ef645-152">`[ProviderName <String>]`: Имя поставщика родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef645-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="ef645-153">`[ResourceGroupName <String>]`: Имя получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef645-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="ef645-154">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="ef645-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="ef645-155">`[ResourceName <String>]`: Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef645-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="ef645-156">`[ResourceType <String>]`: Тип ресурса для родительского ресурса</span><span class="sxs-lookup"><span data-stu-id="ef645-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="ef645-157">`[SolutionName <String>]`: Имя пользовательского решения.</span><span class="sxs-lookup"><span data-stu-id="ef645-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="ef645-158">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ef645-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ef645-159">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ef645-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ef645-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef645-160">RELATED LINKS</span></span>

