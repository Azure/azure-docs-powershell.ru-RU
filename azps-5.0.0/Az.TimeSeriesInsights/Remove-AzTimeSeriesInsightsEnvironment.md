---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249742"
---
# <span data-ttu-id="a6bdc-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="a6bdc-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="a6bdc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="a6bdc-103">Удаление среды с указанным именем в указанной подписке и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="a6bdc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6bdc-104">SYNTAX</span></span>

### <span data-ttu-id="a6bdc-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6bdc-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6bdc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a6bdc-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6bdc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6bdc-107">DESCRIPTION</span></span>
<span data-ttu-id="a6bdc-108">Удаление среды с указанным именем в указанной подписке и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="a6bdc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6bdc-109">EXAMPLES</span></span>

### <span data-ttu-id="a6bdc-110">Пример 1: Удаление среды с представлением временной последовательности по имени</span><span class="sxs-lookup"><span data-stu-id="a6bdc-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="a6bdc-111">Эта команда удаляет среду "аналитика временных рядов".</span><span class="sxs-lookup"><span data-stu-id="a6bdc-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="a6bdc-112">Пример 2: Удаление среды "аналитика временной последовательности" по объекту</span><span class="sxs-lookup"><span data-stu-id="a6bdc-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="a6bdc-113">Эта команда удаляет среду "аналитика временных рядов".</span><span class="sxs-lookup"><span data-stu-id="a6bdc-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="a6bdc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6bdc-114">PARAMETERS</span></span>

### <span data-ttu-id="a6bdc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6bdc-115">-DefaultProfile</span></span>
<span data-ttu-id="a6bdc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6bdc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6bdc-117">-InputObject</span></span>
<span data-ttu-id="a6bdc-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6bdc-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6bdc-119">-Name</span></span>
<span data-ttu-id="a6bdc-120">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6bdc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6bdc-121">-PassThru</span></span>
<span data-ttu-id="a6bdc-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a6bdc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6bdc-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6bdc-124">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a6bdc-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6bdc-125">-SubscriptionId</span></span>
<span data-ttu-id="a6bdc-126">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a6bdc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6bdc-127">-Confirm</span></span>
<span data-ttu-id="a6bdc-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6bdc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6bdc-129">-WhatIf</span></span>
<span data-ttu-id="a6bdc-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6bdc-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6bdc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6bdc-132">CommonParameters</span></span>
<span data-ttu-id="a6bdc-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6bdc-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6bdc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6bdc-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6bdc-135">INPUTS</span></span>

### <span data-ttu-id="a6bdc-136">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a6bdc-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a6bdc-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6bdc-137">OUTPUTS</span></span>

### <span data-ttu-id="a6bdc-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6bdc-138">System.Boolean</span></span>

## <span data-ttu-id="a6bdc-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6bdc-139">NOTES</span></span>

<span data-ttu-id="a6bdc-140">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a6bdc-140">ALIASES</span></span>

<span data-ttu-id="a6bdc-141">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a6bdc-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6bdc-142">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6bdc-143">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6bdc-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a6bdc-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6bdc-145">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a6bdc-146">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="a6bdc-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a6bdc-147">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a6bdc-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="a6bdc-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6bdc-149">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a6bdc-150">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a6bdc-151">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a6bdc-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a6bdc-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6bdc-152">RELATED LINKS</span></span>

