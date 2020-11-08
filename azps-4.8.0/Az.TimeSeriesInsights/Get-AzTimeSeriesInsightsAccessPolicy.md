---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079335"
---
# <span data-ttu-id="bc0d2-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc0d2-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="bc0d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0d2-103">Получает политику доступа с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="bc0d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc0d2-104">SYNTAX</span></span>

### <span data-ttu-id="bc0d2-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc0d2-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc0d2-106">Получить</span><span class="sxs-lookup"><span data-stu-id="bc0d2-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc0d2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc0d2-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc0d2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc0d2-108">DESCRIPTION</span></span>
<span data-ttu-id="bc0d2-109">Получает политику доступа с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="bc0d2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc0d2-110">EXAMPLES</span></span>

### <span data-ttu-id="bc0d2-111">Пример 1: список всех политик доступа в указанной среде</span><span class="sxs-lookup"><span data-stu-id="bc0d2-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="bc0d2-112">Эта команда перечисляет все политики доступа в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="bc0d2-113">Пример 2: получение указанной политики доступа по имени</span><span class="sxs-lookup"><span data-stu-id="bc0d2-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="bc0d2-114">Эта команда получает указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="bc0d2-115">Пример 3: получение указанной политики доступа по объекту</span><span class="sxs-lookup"><span data-stu-id="bc0d2-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="bc0d2-116">Эта команда получает указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="bc0d2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc0d2-117">PARAMETERS</span></span>

### <span data-ttu-id="bc0d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc0d2-118">-DefaultProfile</span></span>
<span data-ttu-id="bc0d2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc0d2-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="bc0d2-120">-EnvironmentName</span></span>
<span data-ttu-id="bc0d2-121">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="bc0d2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc0d2-122">-InputObject</span></span>
<span data-ttu-id="bc0d2-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc0d2-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc0d2-124">-Name</span></span>
<span data-ttu-id="bc0d2-125">Имя политики доступа к временной последовательности, связанной с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="bc0d2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc0d2-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc0d2-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="bc0d2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc0d2-128">-SubscriptionId</span></span>
<span data-ttu-id="bc0d2-129">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="bc0d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0d2-130">CommonParameters</span></span>
<span data-ttu-id="bc0d2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0d2-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc0d2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0d2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc0d2-133">INPUTS</span></span>

### <span data-ttu-id="bc0d2-134">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="bc0d2-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="bc0d2-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc0d2-135">OUTPUTS</span></span>

### <span data-ttu-id="bc0d2-136">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="bc0d2-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="bc0d2-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc0d2-137">NOTES</span></span>

<span data-ttu-id="bc0d2-138">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="bc0d2-138">ALIASES</span></span>

<span data-ttu-id="bc0d2-139">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="bc0d2-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc0d2-140">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc0d2-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc0d2-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="bc0d2-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc0d2-143">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="bc0d2-144">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="bc0d2-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="bc0d2-145">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="bc0d2-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="bc0d2-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc0d2-147">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="bc0d2-148">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="bc0d2-149">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0d2-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="bc0d2-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc0d2-150">RELATED LINKS</span></span>

