---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216689"
---
# <span data-ttu-id="f2aef-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2aef-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="f2aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2aef-102">SYNOPSIS</span></span>
<span data-ttu-id="f2aef-103">Получает политику доступа с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="f2aef-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="f2aef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2aef-104">SYNTAX</span></span>

### <span data-ttu-id="f2aef-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2aef-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2aef-106">Получить</span><span class="sxs-lookup"><span data-stu-id="f2aef-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2aef-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2aef-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2aef-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2aef-108">DESCRIPTION</span></span>
<span data-ttu-id="f2aef-109">Получает политику доступа с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="f2aef-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="f2aef-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2aef-110">EXAMPLES</span></span>

### <span data-ttu-id="f2aef-111">Пример 1. Список всех политик доступа в определенной среде</span><span class="sxs-lookup"><span data-stu-id="f2aef-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="f2aef-112">Эта команда содержит список всех политик доступа, которые находятся в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="f2aef-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="f2aef-113">Пример 2. Получить указанную политику доступа по имени</span><span class="sxs-lookup"><span data-stu-id="f2aef-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="f2aef-114">Эта команда получает указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="f2aef-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="f2aef-115">Пример 3. Получить указанную политику доступа для объекта</span><span class="sxs-lookup"><span data-stu-id="f2aef-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="f2aef-116">Эта команда получает указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="f2aef-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="f2aef-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2aef-117">PARAMETERS</span></span>

### <span data-ttu-id="f2aef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2aef-118">-DefaultProfile</span></span>
<span data-ttu-id="f2aef-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2aef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2aef-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="f2aef-120">-EnvironmentName</span></span>
<span data-ttu-id="f2aef-121">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2aef-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="f2aef-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2aef-122">-InputObject</span></span>
<span data-ttu-id="f2aef-123">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="f2aef-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2aef-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f2aef-124">-Name</span></span>
<span data-ttu-id="f2aef-125">Имя политики доступа к time Series Insights, связанной с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="f2aef-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2aef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2aef-126">-ResourceGroupName</span></span>
<span data-ttu-id="f2aef-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f2aef-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f2aef-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2aef-128">-SubscriptionId</span></span>
<span data-ttu-id="f2aef-129">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="f2aef-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2aef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2aef-130">CommonParameters</span></span>
<span data-ttu-id="f2aef-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2aef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2aef-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2aef-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2aef-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2aef-133">INPUTS</span></span>

### <span data-ttu-id="f2aef-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="f2aef-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="f2aef-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2aef-135">OUTPUTS</span></span>

### <span data-ttu-id="f2aef-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="f2aef-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="f2aef-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2aef-137">NOTES</span></span>

<span data-ttu-id="f2aef-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f2aef-138">ALIASES</span></span>

<span data-ttu-id="f2aef-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="f2aef-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2aef-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="f2aef-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2aef-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2aef-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2aef-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="f2aef-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2aef-143">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="f2aef-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="f2aef-144">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="f2aef-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="f2aef-145">`[EventSourceName <String>]`: имя источника события "Time Series Insights", связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="f2aef-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="f2aef-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="f2aef-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2aef-147">`[ReferenceDataSetName <String>]`: Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="f2aef-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="f2aef-148">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f2aef-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="f2aef-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="f2aef-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f2aef-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2aef-150">RELATED LINKS</span></span>

