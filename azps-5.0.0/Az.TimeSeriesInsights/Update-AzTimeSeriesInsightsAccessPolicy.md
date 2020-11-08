---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245995"
---
# <span data-ttu-id="389d7-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="389d7-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="389d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="389d7-102">SYNOPSIS</span></span>
<span data-ttu-id="389d7-103">Обновляет политику доступа с указанным именем в указанной подписке, группе ресурсов и средой.</span><span class="sxs-lookup"><span data-stu-id="389d7-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="389d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="389d7-104">SYNTAX</span></span>

### <span data-ttu-id="389d7-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="389d7-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="389d7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="389d7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="389d7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="389d7-107">DESCRIPTION</span></span>
<span data-ttu-id="389d7-108">Обновляет политику доступа с указанным именем в указанной подписке, группе ресурсов и средой.</span><span class="sxs-lookup"><span data-stu-id="389d7-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="389d7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="389d7-109">EXAMPLES</span></span>

### <span data-ttu-id="389d7-110">Пример 1: обновление указанной политики доступа по имени</span><span class="sxs-lookup"><span data-stu-id="389d7-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="389d7-111">Эта команда обновляет указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="389d7-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="389d7-112">Пример 2: обновление указанной политики доступа по объекту</span><span class="sxs-lookup"><span data-stu-id="389d7-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="389d7-113">Эта команда обновляет указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="389d7-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="389d7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="389d7-114">PARAMETERS</span></span>

### <span data-ttu-id="389d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="389d7-115">-DefaultProfile</span></span>
<span data-ttu-id="389d7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="389d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="389d7-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="389d7-117">-Description</span></span>
<span data-ttu-id="389d7-118">Описание политики доступа.</span><span class="sxs-lookup"><span data-stu-id="389d7-118">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="389d7-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="389d7-119">-EnvironmentName</span></span>
<span data-ttu-id="389d7-120">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="389d7-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="389d7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="389d7-121">-InputObject</span></span>
<span data-ttu-id="389d7-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="389d7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="389d7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="389d7-123">-Name</span></span>
<span data-ttu-id="389d7-124">Имя политики доступа к временной последовательности, связанной с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="389d7-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="389d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="389d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="389d7-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="389d7-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="389d7-127">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="389d7-127">-Role</span></span>
<span data-ttu-id="389d7-128">Список ролей, назначаемых участником в среде.</span><span class="sxs-lookup"><span data-stu-id="389d7-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="389d7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="389d7-129">-SubscriptionId</span></span>
<span data-ttu-id="389d7-130">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="389d7-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="389d7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="389d7-131">-Confirm</span></span>
<span data-ttu-id="389d7-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="389d7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="389d7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="389d7-133">-WhatIf</span></span>
<span data-ttu-id="389d7-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="389d7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="389d7-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="389d7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="389d7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="389d7-136">CommonParameters</span></span>
<span data-ttu-id="389d7-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="389d7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="389d7-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="389d7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="389d7-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="389d7-139">INPUTS</span></span>

### <span data-ttu-id="389d7-140">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="389d7-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="389d7-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="389d7-141">OUTPUTS</span></span>

### <span data-ttu-id="389d7-142">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="389d7-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="389d7-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="389d7-143">NOTES</span></span>

<span data-ttu-id="389d7-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="389d7-144">ALIASES</span></span>

<span data-ttu-id="389d7-145">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="389d7-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="389d7-146">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="389d7-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="389d7-147">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="389d7-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="389d7-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="389d7-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="389d7-149">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="389d7-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="389d7-150">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="389d7-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="389d7-151">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="389d7-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="389d7-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="389d7-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="389d7-153">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="389d7-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="389d7-154">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="389d7-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="389d7-155">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="389d7-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="389d7-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="389d7-156">RELATED LINKS</span></span>

