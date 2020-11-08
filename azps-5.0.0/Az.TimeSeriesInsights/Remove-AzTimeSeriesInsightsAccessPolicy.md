---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246496"
---
# <span data-ttu-id="6f7c0-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6f7c0-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="6f7c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7c0-103">Удаление политики доступа с указанным именем в указанной подписке, группе ресурсов и окружении.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="6f7c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f7c0-104">SYNTAX</span></span>

### <span data-ttu-id="6f7c0-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f7c0-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6f7c0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6f7c0-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6f7c0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f7c0-107">DESCRIPTION</span></span>
<span data-ttu-id="6f7c0-108">Удаление политики доступа с указанным именем в указанной подписке, группе ресурсов и окружении.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="6f7c0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f7c0-109">EXAMPLES</span></span>

### <span data-ttu-id="6f7c0-110">Пример 1: удаление указанной политики доступа по имени</span><span class="sxs-lookup"><span data-stu-id="6f7c0-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="6f7c0-111">Эта команда удаляет указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="6f7c0-112">Пример 2: удаление указанной политики доступа по объекту</span><span class="sxs-lookup"><span data-stu-id="6f7c0-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="6f7c0-113">Эта команда удаляет указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="6f7c0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f7c0-114">PARAMETERS</span></span>

### <span data-ttu-id="6f7c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7c0-115">-DefaultProfile</span></span>
<span data-ttu-id="6f7c0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f7c0-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="6f7c0-117">-EnvironmentName</span></span>
<span data-ttu-id="6f7c0-118">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="6f7c0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f7c0-119">-InputObject</span></span>
<span data-ttu-id="6f7c0-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6f7c0-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f7c0-121">-Name</span></span>
<span data-ttu-id="6f7c0-122">Имя политики доступа к временной последовательности, связанной с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f7c0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f7c0-123">-PassThru</span></span>
<span data-ttu-id="6f7c0-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6f7c0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f7c0-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f7c0-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="6f7c0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f7c0-127">-SubscriptionId</span></span>
<span data-ttu-id="6f7c0-128">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6f7c0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f7c0-129">-Confirm</span></span>
<span data-ttu-id="6f7c0-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f7c0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f7c0-131">-WhatIf</span></span>
<span data-ttu-id="6f7c0-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f7c0-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f7c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7c0-134">CommonParameters</span></span>
<span data-ttu-id="6f7c0-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7c0-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f7c0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7c0-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f7c0-137">INPUTS</span></span>

### <span data-ttu-id="6f7c0-138">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="6f7c0-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="6f7c0-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f7c0-139">OUTPUTS</span></span>

### <span data-ttu-id="6f7c0-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f7c0-140">System.Boolean</span></span>

## <span data-ttu-id="6f7c0-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f7c0-141">NOTES</span></span>

<span data-ttu-id="6f7c0-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="6f7c0-142">ALIASES</span></span>

<span data-ttu-id="6f7c0-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6f7c0-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6f7c0-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6f7c0-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6f7c0-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="6f7c0-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6f7c0-147">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="6f7c0-148">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="6f7c0-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="6f7c0-149">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="6f7c0-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="6f7c0-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6f7c0-151">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="6f7c0-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="6f7c0-153">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7c0-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6f7c0-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f7c0-154">RELATED LINKS</span></span>

