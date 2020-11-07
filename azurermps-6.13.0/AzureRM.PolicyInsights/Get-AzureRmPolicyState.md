---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyState.md
ms.openlocfilehash: 6f5f1c341db0c5f57ffb541b9455369c0c6e5ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732303"
---
# <span data-ttu-id="2cb63-101">Get-AzureRmPolicyState</span><span class="sxs-lookup"><span data-stu-id="2cb63-101">Get-AzureRmPolicyState</span></span>

## <span data-ttu-id="2cb63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cb63-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb63-103">Возвращает состояние соответствия политике для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cb63-103">Gets policy compliance states for resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cb63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cb63-104">SYNTAX</span></span>

### <span data-ttu-id="2cb63-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2cb63-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb63-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="2cb63-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb63-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="2cb63-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb63-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="2cb63-108">ResourceScope</span></span>
```
Get-AzureRmPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb63-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="2cb63-109">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb63-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="2cb63-110">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb63-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="2cb63-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cb63-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="2cb63-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cb63-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cb63-113">DESCRIPTION</span></span>
<span data-ttu-id="2cb63-114">Возвращает состояние соответствия политике для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cb63-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="2cb63-115">Записи состояния политики можно запрашивать в различных областях.</span><span class="sxs-lookup"><span data-stu-id="2cb63-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="2cb63-116">На основе указанного интервала времени (по умолчанию — последний день) можно запрашивать либо последние состояния политики, либо все переходы состояния политики.</span><span class="sxs-lookup"><span data-stu-id="2cb63-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="2cb63-117">Результаты могут быть вычислены с фильтрацией, группировкой и группировкой.</span><span class="sxs-lookup"><span data-stu-id="2cb63-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="2cb63-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cb63-118">EXAMPLES</span></span>

### <span data-ttu-id="2cb63-119">Пример 1: получение последних состояний политики в текущей области подписки</span><span class="sxs-lookup"><span data-stu-id="2cb63-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState
```

<span data-ttu-id="2cb63-120">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="2cb63-121">Пример 2: получение последних состояний политики в указанной области подписки</span><span class="sxs-lookup"><span data-stu-id="2cb63-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="2cb63-122">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="2cb63-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="2cb63-123">Пример 3: получение всех состояний политики в текущей области подписки</span><span class="sxs-lookup"><span data-stu-id="2cb63-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -All
```

<span data-ttu-id="2cb63-124">Возвращает все записи состояния политики (включая последние), созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="2cb63-125">Пример 4: получение последних состояний политики в области группы управления</span><span class="sxs-lookup"><span data-stu-id="2cb63-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="2cb63-126">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="2cb63-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="2cb63-127">Пример 5: получение последних состояний политики в области "область группы ресурсов" в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="2cb63-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="2cb63-128">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной группе ресурсов (в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="2cb63-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="2cb63-129">Пример 6: получение последних состояний политики в области "Группа ресурсов" в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="2cb63-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="2cb63-130">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="2cb63-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="2cb63-131">Пример 7: получение последних состояний политики для ресурса</span><span class="sxs-lookup"><span data-stu-id="2cb63-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="2cb63-132">Возвращает последние записи состояния политики, созданные за последний день для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="2cb63-133">Пример 8: получение последних состояний политики для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="2cb63-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="2cb63-134">Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="2cb63-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="2cb63-135">Пример 9: получение последних состояний политики для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="2cb63-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="2cb63-136">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="2cb63-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="2cb63-137">Пример 10: получение последних состояний политики для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="2cb63-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="2cb63-138">Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="2cb63-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="2cb63-139">Пример 11: получение последних состояний политики для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="2cb63-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="2cb63-140">Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="2cb63-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="2cb63-141">Пример 12: получение последних состояний политики для назначения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="2cb63-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="2cb63-142">Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (оно существует в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="2cb63-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="2cb63-143">Пример 13: получение последних состояний политики для назначения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="2cb63-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="2cb63-144">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="2cb63-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="2cb63-145">Пример 14: получение последних состояний политики для назначения политики в указанной группе ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="2cb63-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="2cb63-146">Возвращает последние записи состояния политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в группе ресурсов в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="2cb63-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="2cb63-147">Пример 15: получение последних состояний политики в текущей области подписки с параметрами OrderBy, Top и SELECT запроса</span><span class="sxs-lookup"><span data-stu-id="2cb63-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="2cb63-148">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="2cb63-149">Команда упорядочивает результаты по свойствам timestamp и Name назначения политики и занимает только первые 5 из указанных в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="2cb63-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="2cb63-150">Он также выберет для списка только подмножество столбцов для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="2cb63-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="2cb63-151">Пример 16: получение последних состояний политики в текущей области подписки с параметрами "из" и "по запросу"</span><span class="sxs-lookup"><span data-stu-id="2cb63-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="2cb63-152">Возвращает последние записи состояния политики, созданные в диапазоне дат, указанном для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="2cb63-153">Пример 17: получение последних состояний политики в текущей области подписки с помощью параметра "Фильтрация запроса"</span><span class="sxs-lookup"><span data-stu-id="2cb63-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and IsCompliant eq false and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="2cb63-154">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="2cb63-155">Команда ограничивает результаты, возвращаемые фильтром, на основе действия, связанного с определением политики (в том числе действия запрета или аудита), состояния соответствия (включает только состояние "не соответствует требованиям") и расположения ресурса (исключает расположение eastus).</span><span class="sxs-lookup"><span data-stu-id="2cb63-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="2cb63-156">Пример 18: получение последних состояний политики в текущей области подписок с применением функции определения агрегата количества строк</span><span class="sxs-lookup"><span data-stu-id="2cb63-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="2cb63-157">Получает количество последних записей состояния политики, созданных за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="2cb63-158">Команда возвращает количество записей состояния политики, которое возвращается в рамках свойства AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="2cb63-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="2cb63-159">Пример 19: получение последних состояний политики в текущей области подписки с применением задания группировки с агрегированием</span><span class="sxs-lookup"><span data-stu-id="2cb63-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="2cb63-160">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="2cb63-161">Команда ограничивает результаты, возвращаемые фильтром, на основе состояния соответствия требованиям (включает только состояние "не соответствует требованиям").</span><span class="sxs-lookup"><span data-stu-id="2cb63-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="2cb63-162">Результаты группируются на основе назначения политики, определения политики и определения политики, а также вычисляется количество записей в каждой группе, которое возвращается в рамках свойства AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="2cb63-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="2cb63-163">Результаты статистического выражения упорядочиваются по убыванию и выполняются только первые 5 из указанных в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="2cb63-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="2cb63-164">Пример 20: получение последних состояний политики в текущей области подписки с применением задания группирования без агрегата</span><span class="sxs-lookup"><span data-stu-id="2cb63-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="2cb63-165">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="2cb63-166">Команда ограничивает результаты, возвращаемые фильтром, на основе состояния соответствия требованиям (включает только состояние "не соответствует требованиям").</span><span class="sxs-lookup"><span data-stu-id="2cb63-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="2cb63-167">Результаты группируются на основе идентификатора ресурса. Это приведет к формированию списка всех ресурсов в подписке, которые не соответствуют требованиям хотя бы одной политики.</span><span class="sxs-lookup"><span data-stu-id="2cb63-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="2cb63-168">Пример 21: получение последних состояний политики в текущей области подписки с применением задания нескольких групп</span><span class="sxs-lookup"><span data-stu-id="2cb63-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyState -Filter "IsCompliant eq false" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

<span data-ttu-id="2cb63-169">Возвращает последние записи состояния политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-169">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="2cb63-170">Команда ограничивает результаты, возвращаемые фильтром, на основе состояния соответствия требованиям (включает только состояние "не соответствует требованиям").</span><span class="sxs-lookup"><span data-stu-id="2cb63-170">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="2cb63-171">Результаты сначала группируются в соответствии с назначением политики, определением политики, определением политики и идентификатором ресурса. Затем он дополнительно группирует результаты этого группирования с теми же свойствами, но за исключением идентификатора ресурса, и вычисляет количество записей в каждой из этих групп, которое возвращается в рамках свойства AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="2cb63-171">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="2cb63-172">Результаты статистического выражения упорядочиваются по убыванию и выполняются только первые 5 из указанных в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="2cb63-172">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="2cb63-173">Это приведет к формированию 5 основных политик с наибольшим количеством несоответствующих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cb63-173">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="2cb63-174">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cb63-174">PARAMETERS</span></span>

### <span data-ttu-id="2cb63-175">-ALL</span><span class="sxs-lookup"><span data-stu-id="2cb63-175">-All</span></span>
<span data-ttu-id="2cb63-176">Выводит все состояния политики в течение заданного интервала времени, а не только самую последнюю.</span><span class="sxs-lookup"><span data-stu-id="2cb63-176">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="2cb63-177">-Apply (Применить)</span><span class="sxs-lookup"><span data-stu-id="2cb63-177">-Apply</span></span>
<span data-ttu-id="2cb63-178">Применение выражения для агрегатов с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="2cb63-178">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="2cb63-179">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb63-179">-DefaultProfile</span></span>
<span data-ttu-id="2cb63-180">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb63-180">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb63-181">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="2cb63-181">-Filter</span></span>
<span data-ttu-id="2cb63-182">Выражение фильтра с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="2cb63-182">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="2cb63-183">-From</span><span class="sxs-lookup"><span data-stu-id="2cb63-183">-From</span></span>
<span data-ttu-id="2cb63-184">Отформатированная отметка времени ISO 8601 с указанием времени начала интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-184">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="2cb63-185">Если не указано, по умолчанию используется значение параметра "до" за вычетом 1 дня.</span><span class="sxs-lookup"><span data-stu-id="2cb63-185">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="2cb63-186">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb63-186">-ManagementGroupName</span></span>
<span data-ttu-id="2cb63-187">Имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="2cb63-187">Management group name.</span></span>

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

### <span data-ttu-id="2cb63-188">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="2cb63-188">-OrderBy</span></span>
<span data-ttu-id="2cb63-189">Выражение упорядочивания с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="2cb63-189">Ordering expression using OData notation.</span></span>
<span data-ttu-id="2cb63-190">Одно или несколько имен столбцов с разделителями-запятыми с дополнительным аргументом "DESC" (значение по умолчанию) или "ASC".</span><span class="sxs-lookup"><span data-stu-id="2cb63-190">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="2cb63-191">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="2cb63-191">-PolicyAssignmentName</span></span>
<span data-ttu-id="2cb63-192">Имя назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2cb63-192">Policy assignment name.</span></span>

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

### <span data-ttu-id="2cb63-193">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2cb63-193">-PolicyDefinitionName</span></span>
<span data-ttu-id="2cb63-194">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="2cb63-194">Policy definition name.</span></span>

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

### <span data-ttu-id="2cb63-195">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2cb63-195">-PolicySetDefinitionName</span></span>
<span data-ttu-id="2cb63-196">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="2cb63-196">Policy set definition name.</span></span>

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

### <span data-ttu-id="2cb63-197">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb63-197">-ResourceGroupName</span></span>
<span data-ttu-id="2cb63-198">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cb63-198">Resource group name.</span></span>

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

### <span data-ttu-id="2cb63-199">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cb63-199">-ResourceId</span></span>
<span data-ttu-id="2cb63-200">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-200">Resource ID.</span></span>

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

### <span data-ttu-id="2cb63-201">-SELECT</span><span class="sxs-lookup"><span data-stu-id="2cb63-201">-Select</span></span>
<span data-ttu-id="2cb63-202">Выберите выражение с помощью нотации OData.</span><span class="sxs-lookup"><span data-stu-id="2cb63-202">Select expression using OData notation.</span></span>
<span data-ttu-id="2cb63-203">Одно или несколько имен столбцов с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="2cb63-203">One or more comma-separated column names.</span></span>
<span data-ttu-id="2cb63-204">Ограничивает столбцы каждой записи только запрошенными.</span><span class="sxs-lookup"><span data-stu-id="2cb63-204">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="2cb63-205">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2cb63-205">-SubscriptionId</span></span>
<span data-ttu-id="2cb63-206">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="2cb63-206">Subscription ID.</span></span>

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

### <span data-ttu-id="2cb63-207">-To</span><span class="sxs-lookup"><span data-stu-id="2cb63-207">-To</span></span>
<span data-ttu-id="2cb63-208">Отформатированная отметка времени ISO 8601, указывающая время окончания интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-208">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="2cb63-209">Если не указано, по умолчанию используется время запроса.</span><span class="sxs-lookup"><span data-stu-id="2cb63-209">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="2cb63-210">-Top</span><span class="sxs-lookup"><span data-stu-id="2cb63-210">-Top</span></span>
<span data-ttu-id="2cb63-211">Максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="2cb63-211">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="2cb63-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb63-212">CommonParameters</span></span>
<span data-ttu-id="2cb63-213">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cb63-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb63-214">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cb63-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb63-215">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cb63-215">INPUTS</span></span>

### <span data-ttu-id="2cb63-216">System. String</span><span class="sxs-lookup"><span data-stu-id="2cb63-216">System.String</span></span>

## <span data-ttu-id="2cb63-217">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cb63-217">OUTPUTS</span></span>

### <span data-ttu-id="2cb63-218">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyState</span><span class="sxs-lookup"><span data-stu-id="2cb63-218">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="2cb63-219">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cb63-219">NOTES</span></span>

## <span data-ttu-id="2cb63-220">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cb63-220">RELATED LINKS</span></span>

[<span data-ttu-id="2cb63-221">Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="2cb63-221">Get-AzureRmPolicyStateSummary</span></span>](./Get-AzureRmPolicyStateSummary.md)
