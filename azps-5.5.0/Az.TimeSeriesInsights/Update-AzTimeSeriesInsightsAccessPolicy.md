---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231345"
---
# <span data-ttu-id="dfe9b-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dfe9b-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="dfe9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfe9b-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe9b-103">Обновляет политику доступа с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="dfe9b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dfe9b-104">SYNTAX</span></span>

### <span data-ttu-id="dfe9b-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfe9b-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dfe9b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dfe9b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dfe9b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfe9b-107">DESCRIPTION</span></span>
<span data-ttu-id="dfe9b-108">Обновляет политику доступа с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="dfe9b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dfe9b-109">EXAMPLES</span></span>

### <span data-ttu-id="dfe9b-110">Пример 1. Обновление указанной политики доступа по имени</span><span class="sxs-lookup"><span data-stu-id="dfe9b-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="dfe9b-111">Эта команда обновляет указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="dfe9b-112">Пример 2. Обновление указанной политики доступа для объекта</span><span class="sxs-lookup"><span data-stu-id="dfe9b-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="dfe9b-113">Эта команда обновляет указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="dfe9b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfe9b-114">PARAMETERS</span></span>

### <span data-ttu-id="dfe9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe9b-115">-DefaultProfile</span></span>
<span data-ttu-id="dfe9b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfe9b-117">-Description</span><span class="sxs-lookup"><span data-stu-id="dfe9b-117">-Description</span></span>
<span data-ttu-id="dfe9b-118">Описание политики доступа.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="dfe9b-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="dfe9b-119">-EnvironmentName</span></span>
<span data-ttu-id="dfe9b-120">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="dfe9b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfe9b-121">-InputObject</span></span>
<span data-ttu-id="dfe9b-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dfe9b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dfe9b-123">-Name</span></span>
<span data-ttu-id="dfe9b-124">Имя политики доступа "Time Series Insights", связанной с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="dfe9b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe9b-125">-ResourceGroupName</span></span>
<span data-ttu-id="dfe9b-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="dfe9b-127">-Роль</span><span class="sxs-lookup"><span data-stu-id="dfe9b-127">-Role</span></span>
<span data-ttu-id="dfe9b-128">Список ролей, которые назначены основной в среде.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-128">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="dfe9b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfe9b-129">-SubscriptionId</span></span>
<span data-ttu-id="dfe9b-130">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="dfe9b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfe9b-131">-Confirm</span></span>
<span data-ttu-id="dfe9b-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfe9b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe9b-133">-WhatIf</span></span>
<span data-ttu-id="dfe9b-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfe9b-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfe9b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe9b-136">CommonParameters</span></span>
<span data-ttu-id="dfe9b-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe9b-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfe9b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe9b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfe9b-139">INPUTS</span></span>

### <span data-ttu-id="dfe9b-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="dfe9b-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="dfe9b-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dfe9b-141">OUTPUTS</span></span>

### <span data-ttu-id="dfe9b-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="dfe9b-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="dfe9b-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dfe9b-143">NOTES</span></span>

<span data-ttu-id="dfe9b-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dfe9b-144">ALIASES</span></span>

<span data-ttu-id="dfe9b-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="dfe9b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dfe9b-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfe9b-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dfe9b-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="dfe9b-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dfe9b-149">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="dfe9b-150">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="dfe9b-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="dfe9b-151">`[EventSourceName <String>]`: имя источника события "Time Series Insights", связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="dfe9b-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="dfe9b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dfe9b-153">`[ReferenceDataSetName <String>]`: имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="dfe9b-154">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="dfe9b-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="dfe9b-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="dfe9b-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfe9b-156">RELATED LINKS</span></span>

