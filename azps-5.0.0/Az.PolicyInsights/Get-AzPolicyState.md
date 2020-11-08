---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246869"
---
# <span data-ttu-id="871bf-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="871bf-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="871bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="871bf-102">SYNOPSIS</span></span>
<span data-ttu-id="871bf-103">Возвращает состояние соответствия политике для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="871bf-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="871bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="871bf-104">SYNTAX</span></span>

### <span data-ttu-id="871bf-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="871bf-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="871bf-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="871bf-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="871bf-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="871bf-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="871bf-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="871bf-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="871bf-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="871bf-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="871bf-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="871bf-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="871bf-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="871bf-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="871bf-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="871bf-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="871bf-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="871bf-113">DESCRIPTION</span></span>
<span data-ttu-id="871bf-114">Возвращает состояние соответствия политике для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="871bf-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="871bf-115">Записи состояния политики можно запрашивать в различных областях.</span><span class="sxs-lookup"><span data-stu-id="871bf-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="871bf-116">На основе указанного интервала времени (по умолчанию — последний день) можно запрашивать либо последние состояния политики, либо все переходы состояния политики.</span><span class="sxs-lookup"><span data-stu-id="871bf-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="871bf-117">Результаты могут быть вычислены с фильтрацией, группировкой и группировкой.</span><span class="sxs-lookup"><span data-stu-id="871bf-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="871bf-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="871bf-118">EXAMPLES</span></span>

### <span data-ttu-id="871bf-119">Пример 1: получение последних состояний политики в текущей области подписки</span><span class="sxs-lookup"><span data-stu-id="871bf-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="871bf-120">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="871bf-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="871bf-121">Пример 2: получение последних состояний политики в указанной области подписки</span><span class="sxs-lookup"><span data-stu-id="871bf-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="871bf-122">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="871bf-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="871bf-123">Пример 3: получение всех состояний политики в текущей области подписки</span><span class="sxs-lookup"><span data-stu-id="871bf-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="871bf-124">Возвращает все записи состояния политики (включая последние), созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="871bf-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="871bf-125">Пример 4: получение последних состояний политики в области группы управления</span><span class="sxs-lookup"><span data-stu-id="871bf-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="871bf-126">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="871bf-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="871bf-127">Пример 5: получение последних состояний политики в области "область группы ресурсов" в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="871bf-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="871bf-128">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной группе ресурсов (в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="871bf-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="871bf-129">Пример 6: получение последних состояний политики в области "Группа ресурсов" в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="871bf-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="871bf-130">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="871bf-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="871bf-131">Пример 7: получение последних состояний политики для ресурса</span><span class="sxs-lookup"><span data-stu-id="871bf-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="871bf-132">Возвращает последние записи состояния политики, созданные за последний день для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="871bf-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="871bf-133">Пример 8: получение последних состояний политики для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="871bf-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="871bf-134">Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="871bf-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="871bf-135">Пример 9: получение последних состояний политики для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="871bf-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="871bf-136">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="871bf-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="871bf-137">Пример 10: получение последних состояний политики для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="871bf-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="871bf-138">Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="871bf-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="871bf-139">Пример 11: получение последних состояний политики для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="871bf-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="871bf-140">Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="871bf-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="871bf-141">Пример 12: получение последних состояний политики для назначения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="871bf-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="871bf-142">Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (оно существует в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="871bf-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="871bf-143">Пример 13: получение последних состояний политики для назначения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="871bf-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="871bf-144">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="871bf-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="871bf-145">Пример 14: получение последних состояний политики для назначения политики в указанной группе ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="871bf-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="871bf-146">Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в группе ресурсов в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="871bf-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="871bf-147">Пример 15: получение последних состояний политики в текущей области подписки с параметрами OrderBy, Top и SELECT запроса</span><span class="sxs-lookup"><span data-stu-id="871bf-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="871bf-148">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="871bf-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="871bf-149">Команда упорядочивает результаты по свойствам timestamp и Name назначения политики и занимает только первые 5 из указанных в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="871bf-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="871bf-150">Он также выберет для списка только подмножество столбцов для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="871bf-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="871bf-151">Пример 16: получение последних состояний политики в текущей области подписки с параметрами "из" и "по запросу"</span><span class="sxs-lookup"><span data-stu-id="871bf-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="871bf-152">Возвращает последние записи состояния политики, созданные в диапазоне дат, указанном для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="871bf-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="871bf-153">Пример 17: получение последних состояний политики в текущей области подписки с помощью параметра "Фильтрация запроса"</span><span class="sxs-lookup"><span data-stu-id="871bf-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="871bf-154">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="871bf-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="871bf-155">Команда ограничивает результаты, возвращаемые фильтром, на основе действия, связанного с определением политики (в том числе действия запрета или аудита), состояния соответствия (включает только состояние "не соответствует требованиям") и расположения ресурса (исключает расположение eastus).</span><span class="sxs-lookup"><span data-stu-id="871bf-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="871bf-156">Пример 18: получение последних состояний политики в текущей области подписок с применением функции определения агрегата количества строк</span><span class="sxs-lookup"><span data-stu-id="871bf-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="871bf-157">Получает количество последних записей состояния политики, созданных за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="871bf-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="871bf-158">Команда возвращает количество записей состояния политики, которое возвращается в рамках свойства AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="871bf-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="871bf-159">Пример 19: получение последних состояний политики в текущей области подписки с применением задания группировки с агрегированием</span><span class="sxs-lookup"><span data-stu-id="871bf-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="871bf-160">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="871bf-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="871bf-161">Команда ограничивает результаты, возвращаемые фильтром, на основе состояния соответствия требованиям (включает только состояние "не соответствует требованиям").</span><span class="sxs-lookup"><span data-stu-id="871bf-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="871bf-162">Результаты группируются на основе назначения политики, определения политики и определения политики, а также вычисляется количество записей в каждой группе, которое возвращается в рамках свойства AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="871bf-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="871bf-163">Результаты статистического выражения упорядочиваются по убыванию и выполняются только первые 5 из указанных в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="871bf-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="871bf-164">Пример 20: получение последних состояний политики в текущей области подписки с применением задания группирования без агрегата</span><span class="sxs-lookup"><span data-stu-id="871bf-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="871bf-165">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="871bf-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="871bf-166">Команда ограничивает результаты, возвращаемые фильтром, на основе состояния соответствия требованиям (включает только состояние "не соответствует требованиям").</span><span class="sxs-lookup"><span data-stu-id="871bf-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="871bf-167">Результаты группируются на основе идентификатора ресурса. Это приведет к формированию списка всех ресурсов в подписке, которые не соответствуют требованиям хотя бы одной политики.</span><span class="sxs-lookup"><span data-stu-id="871bf-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="871bf-168">Пример 21: получение последних состояний политики в текущей области подписки с применением задания нескольких групп</span><span class="sxs-lookup"><span data-stu-id="871bf-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="871bf-169">Пример 22: получение последних состояний политики, включая сведения об оценке политики для ресурса</span><span class="sxs-lookup"><span data-stu-id="871bf-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="871bf-170">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="871bf-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="871bf-171">Команда ограничивает результаты, возвращаемые фильтром, на основе состояния соответствия требованиям (включает только состояние "не соответствует требованиям").</span><span class="sxs-lookup"><span data-stu-id="871bf-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="871bf-172">Результаты сначала группируются в соответствии с назначением политики, определением политики, определением политики и идентификатором ресурса. Затем он дополнительно группирует результаты этого группирования с теми же свойствами, но за исключением идентификатора ресурса, и вычисляет количество записей в каждой из этих групп, которое возвращается в рамках свойства AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="871bf-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="871bf-173">Результаты статистического выражения упорядочиваются по убыванию и выполняются только первые 5 из указанных в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="871bf-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="871bf-174">Это приведет к формированию 5 основных политик с наибольшим количеством несоответствующих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="871bf-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="871bf-175">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="871bf-175">PARAMETERS</span></span>

### <span data-ttu-id="871bf-176">-ALL</span><span class="sxs-lookup"><span data-stu-id="871bf-176">-All</span></span>
<span data-ttu-id="871bf-177">Выводит все состояния политики в течение заданного интервала времени, а не только самую последнюю.</span><span class="sxs-lookup"><span data-stu-id="871bf-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="871bf-178">-Apply (Применить)</span><span class="sxs-lookup"><span data-stu-id="871bf-178">-Apply</span></span>
<span data-ttu-id="871bf-179">Применение выражения для агрегатов с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="871bf-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="871bf-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871bf-180">-DefaultProfile</span></span>
<span data-ttu-id="871bf-181">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="871bf-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-182">-Expand</span><span class="sxs-lookup"><span data-stu-id="871bf-182">-Expand</span></span>
<span data-ttu-id="871bf-183">Развертывание выражения с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="871bf-183">Expand expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-184">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="871bf-184">-Filter</span></span>
<span data-ttu-id="871bf-185">Выражение фильтра с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="871bf-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="871bf-186">-From</span><span class="sxs-lookup"><span data-stu-id="871bf-186">-From</span></span>
<span data-ttu-id="871bf-187">Отформатированная отметка времени ISO 8601 с указанием времени начала интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="871bf-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="871bf-188">Если не указано, по умолчанию используется значение параметра "до" за вычетом 1 дня.</span><span class="sxs-lookup"><span data-stu-id="871bf-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="871bf-189">-ManagementGroupName</span></span>
<span data-ttu-id="871bf-190">Имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="871bf-190">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="871bf-191">-OrderBy</span></span>
<span data-ttu-id="871bf-192">Выражение упорядочивания с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="871bf-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="871bf-193">Одно или несколько имен столбцов с разделителями-запятыми с дополнительным аргументом "DESC" (значение по умолчанию) или "ASC".</span><span class="sxs-lookup"><span data-stu-id="871bf-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="871bf-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="871bf-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="871bf-195">Имя назначения политики.</span><span class="sxs-lookup"><span data-stu-id="871bf-195">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="871bf-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="871bf-197">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="871bf-197">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="871bf-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="871bf-199">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="871bf-199">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="871bf-200">-ResourceGroupName</span></span>
<span data-ttu-id="871bf-201">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="871bf-201">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="871bf-202">-ResourceId</span></span>
<span data-ttu-id="871bf-203">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="871bf-203">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-204">-SELECT</span><span class="sxs-lookup"><span data-stu-id="871bf-204">-Select</span></span>
<span data-ttu-id="871bf-205">Выберите выражение с помощью нотации OData.</span><span class="sxs-lookup"><span data-stu-id="871bf-205">Select expression using OData notation.</span></span>
<span data-ttu-id="871bf-206">Одно или несколько имен столбцов с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="871bf-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="871bf-207">Ограничивает столбцы каждой записи только запрошенными.</span><span class="sxs-lookup"><span data-stu-id="871bf-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="871bf-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="871bf-208">-SubscriptionId</span></span>
<span data-ttu-id="871bf-209">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="871bf-209">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-210">-To</span><span class="sxs-lookup"><span data-stu-id="871bf-210">-To</span></span>
<span data-ttu-id="871bf-211">Отформатированная отметка времени ISO 8601, указывающая время окончания интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="871bf-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="871bf-212">Если не указано, по умолчанию используется время запроса.</span><span class="sxs-lookup"><span data-stu-id="871bf-212">When not specified, defaults to time of request.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-213">-Top</span><span class="sxs-lookup"><span data-stu-id="871bf-213">-Top</span></span>
<span data-ttu-id="871bf-214">Максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="871bf-214">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871bf-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871bf-215">CommonParameters</span></span>
<span data-ttu-id="871bf-216">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="871bf-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871bf-217">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="871bf-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871bf-218">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="871bf-218">INPUTS</span></span>

### <span data-ttu-id="871bf-219">System. String</span><span class="sxs-lookup"><span data-stu-id="871bf-219">System.String</span></span>

## <span data-ttu-id="871bf-220">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="871bf-220">OUTPUTS</span></span>

### <span data-ttu-id="871bf-221">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyState</span><span class="sxs-lookup"><span data-stu-id="871bf-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="871bf-222">Пуск</span><span class="sxs-lookup"><span data-stu-id="871bf-222">NOTES</span></span>

## <span data-ttu-id="871bf-223">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="871bf-223">RELATED LINKS</span></span>

[<span data-ttu-id="871bf-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="871bf-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
