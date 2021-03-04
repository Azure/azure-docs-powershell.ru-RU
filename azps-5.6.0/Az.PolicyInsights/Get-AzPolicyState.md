---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 82aa08a3d4b4eb42638e1b9def55b5d936f176b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989092"
---
# <span data-ttu-id="8c8ee-101">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="8c8ee-101">Get-AzPolicyState</span></span>

## <span data-ttu-id="8c8ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8ee-103">Возвращает состояния соответствия политике для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-103">Gets policy compliance states for resources.</span></span>

## <span data-ttu-id="8c8ee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c8ee-104">SYNTAX</span></span>

### <span data-ttu-id="8c8ee-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c8ee-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8ee-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="8c8ee-106">ManagementGroupScope</span></span>
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8ee-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="8c8ee-107">ResourceGroupScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8ee-108">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="8c8ee-108">ResourceScope</span></span>
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8ee-109">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="8c8ee-109">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8ee-110">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="8c8ee-110">PolicyDefinitionScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8ee-111">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="8c8ee-111">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8ee-112">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="8c8ee-112">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c8ee-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c8ee-113">DESCRIPTION</span></span>
<span data-ttu-id="8c8ee-114">Возвращает состояния соответствия политике для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-114">Gets policy compliance states for resources.</span></span> <span data-ttu-id="8c8ee-115">Записи состояния политики можно запрашивать в различных областях.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-115">Policy state records can be queried at various scopes.</span></span> <span data-ttu-id="8c8ee-116">В зависимости от заданного интервала времени (по умолчанию — последний день) можно запрашивать последние состояния политики или все переходы между состояниями политики.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-116">Based on the time interval specified (defaults to last day), either latest policy states or all policy state transitions can be queried.</span></span> <span data-ttu-id="8c8ee-117">Результаты можно вычислять с фильтрацией, группировкой и групповыми агрегатами.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-117">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="8c8ee-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c8ee-118">EXAMPLES</span></span>

### <span data-ttu-id="8c8ee-119">Пример 1. Последние состояния политики в текущей области действия подписки</span><span class="sxs-lookup"><span data-stu-id="8c8ee-119">Example 1: Get latest policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState
```

<span data-ttu-id="8c8ee-120">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-120">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="8c8ee-121">Пример 2. Последние состояния политики в указанной области подписки</span><span class="sxs-lookup"><span data-stu-id="8c8ee-121">Example 2: Get latest policy states in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="8c8ee-122">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-122">Gets latest policy state records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="8c8ee-123">Пример 3. Просмотр всех областей политики в текущей области действия подписки</span><span class="sxs-lookup"><span data-stu-id="8c8ee-123">Example 3: Get all policy states in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -All
```

<span data-ttu-id="8c8ee-124">Возвращает все исторические записи об условиях политики (включая последние), созданные в последний день для всех ресурсов подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-124">Gets all historical policy state records (including latest) generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="8c8ee-125">Пример 4. Последние состояния политики в области групп управления</span><span class="sxs-lookup"><span data-stu-id="8c8ee-125">Example 4: Get latest policy states in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="8c8ee-126">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-126">Gets latest policy state records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="8c8ee-127">Пример 5. Последние состояния политики в области группы ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="8c8ee-127">Example 5: Get latest policy states in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="8c8ee-128">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в указанной группе ресурсов (в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-128">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="8c8ee-129">Пример 6. Последние состояния политики в области группы ресурсов в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="8c8ee-129">Example 6: Get latest policy states in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="8c8ee-130">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-130">Gets latest policy state records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="8c8ee-131">Пример 7. Последние состояния политики для ресурса</span><span class="sxs-lookup"><span data-stu-id="8c8ee-131">Example 7: Get latest policy states for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="8c8ee-132">Возвращает последние записи состояния политики, созданные в последний день для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-132">Gets latest policy state records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="8c8ee-133">Пример 8. Определение последних состояния политики для определения набора политик в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="8c8ee-133">Example 8: Get latest policy states for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c8ee-134">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), на которые влияет указанное определение набора политики (которое существует в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-134">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="8c8ee-135">Пример 9. Получите последние состояния политики для определения набора политик в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="8c8ee-135">Example 9: Get latest policy states for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c8ee-136">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), на которые влияет указанное определение набора политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-136">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="8c8ee-137">Пример 10. Последние состояния политики для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="8c8ee-137">Example 10: Get latest policy states for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c8ee-138">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), на которые влияет указанное определение политики (которое существует в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-138">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="8c8ee-139">Пример 11. Просмотр последних состояния политики для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="8c8ee-139">Example 11: Get latest policy states for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="8c8ee-140">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), на которые влияет указанное определение политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-140">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="8c8ee-141">Пример 12. Получать последние состояния политики для назначения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="8c8ee-141">Example 12: Get latest policy states for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="8c8ee-142">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), к работе с помощью указанного назначения политики (которое существует в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-142">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="8c8ee-143">Пример 13. Получать последние состояния политики для назначения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="8c8ee-143">Example 13: Get latest policy states for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="8c8ee-144">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), к работе с помощью указанного назначения политики (существующего в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-144">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="8c8ee-145">Пример 14. Получать последние состояния политики для назначения политики в указанной группе ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="8c8ee-145">Example 14: Get latest policy states for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="8c8ee-146">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов (в пределах клиента в текущем сеансе), к данным о назначении политики (которые существуют в группе ресурсов в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-146">Gets latest policy state records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="8c8ee-147">Пример 15. Последние состояния политики в текущей области действия подписки с вариантами запроса OrderBy, Top и Select</span><span class="sxs-lookup"><span data-stu-id="8c8ee-147">Example 15: Get latest policy states in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

<span data-ttu-id="8c8ee-148">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-148">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c8ee-149">Эта команда отбирает результаты по свойствам timestamp и policy assignment (Имя назначения политики) и отбирает только 5 из 5 перечислены в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-149">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="8c8ee-150">Кроме того, для каждой записи будет выбрано только подмножество столбцов.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-150">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="8c8ee-151">Пример 16. Последние состояния политики в текущей области действия подписки с помощью параметров запроса "От" и "На"</span><span class="sxs-lookup"><span data-stu-id="8c8ee-151">Example 16: Get latest policy states in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="8c8ee-152">Возвращает последние записи состояния политики, созданные в диапазоне дат, указанном для всех ресурсов подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-152">Gets latest policy state records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="8c8ee-153">Пример 17. Последние состояния политики в текущей области подписки с параметром "Фильтровать запрос"</span><span class="sxs-lookup"><span data-stu-id="8c8ee-153">Example 17: Get latest policy states in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="8c8ee-154">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-154">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="8c8ee-155">Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая действия запрета или аудита), состояния соответствия (включая только состояние, не соответствует требованиям) и расположения ресурсов (за исключением расположения на востоке).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-155">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), compliance status (includes only non-compliant status) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="8c8ee-156">Пример 18. Получение последних состояния политики в текущей области подписки с указанием агрегата "Применить" для подсчета строк</span><span class="sxs-lookup"><span data-stu-id="8c8ee-156">Example 18: Get latest policy states in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="8c8ee-157">Возвращает количество последних записей состояния политики, созданных в последний день для всех ресурсов подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-157">Gets the number of latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="8c8ee-158">Команда возвращает количество только записей состояния политики, которое возвращается в свойстве AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-158">The command returns the count of the policy state records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="8c8ee-159">Пример 19. Получение последних состояния политики в текущей области действия подписки с указанием группировки с агрегатом</span><span class="sxs-lookup"><span data-stu-id="8c8ee-159">Example 19: Get latest policy states in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

<span data-ttu-id="8c8ee-160">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-160">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c8ee-161">Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе состояния соответствия требованиям (включая только состояние, не соответствует требованиям).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-161">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="8c8ee-162">Она группирует результаты на основе назначения политики, определения набора политик и определения политики, а также вычисляет количество записей в каждой группе, которое возвращается в свойстве AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-162">It groups the results based on policy assignment, policy set definition, and policy definition, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="8c8ee-163">Она заказывает результаты по агрегату в порядке убыения и принимает только пять лучших из перечислены в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-163">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="8c8ee-164">Пример 20. Получение последних состояния политики в текущей области подписки с указанием группировки без агрегирования</span><span class="sxs-lookup"><span data-stu-id="8c8ee-164">Example 20: Get latest policy states in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="8c8ee-165">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-165">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c8ee-166">Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе состояния соответствия требованиям (включая только состояние, не соответствует требованиям).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-166">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="8c8ee-167">Результаты группируются на основе ид ресурса. При этом создается список всех ресурсов в подписке, которые не соответствуют хотя бы одной политике.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-167">It groups the results based on resource id. This generates the list of all resources within the subscription that are non-compliant for at least one policy.</span></span>

### <span data-ttu-id="8c8ee-168">Пример 21. Получение последних областей политики в текущей области действия подписки с указанием нескольких групп</span><span class="sxs-lookup"><span data-stu-id="8c8ee-168">Example 21: Get latest policy states in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### <span data-ttu-id="8c8ee-169">Пример 22. Сведения о последних состояниях политики, включая сведения о оценке политики для ресурса</span><span class="sxs-lookup"><span data-stu-id="8c8ee-169">Example 22: Get latest policy states including policy evaluation details for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

<span data-ttu-id="8c8ee-170">Возвращает последние записи состояния политики, созданные в последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-170">Gets latest policy state records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="8c8ee-171">Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе состояния соответствия требованиям (включая только состояние, не соответствует требованиям).</span><span class="sxs-lookup"><span data-stu-id="8c8ee-171">The command limits the results returned by filtering based on compliance status (includes only non-compliant status).</span></span>
<span data-ttu-id="8c8ee-172">Сначала результаты группируются на основе назначения политики, определения набора политики, определения политики и ид ресурса. Затем она затем группирует результаты этой группировки с такими же свойствами, за исключением ид ресурса, и вычисляет количество записей в каждой из этих групп, возвращаемого в свойстве AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-172">It groups the results first based on policy assignment, policy set definition, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="8c8ee-173">Она упорядочена по результатам подсчета в порядке убывления и занимает только 5 лучших из перечислены в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-173">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="8c8ee-174">При этом будут создаваться 5 политик с большим количеством несовместимых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-174">This generates the top 5 policies with the most number of non-compliant resources.</span></span>

## <span data-ttu-id="8c8ee-175">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c8ee-175">PARAMETERS</span></span>

### <span data-ttu-id="8c8ee-176">-Все</span><span class="sxs-lookup"><span data-stu-id="8c8ee-176">-All</span></span>
<span data-ttu-id="8c8ee-177">В течение заданного интервала получите все состояния политики, а не только последние.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-177">Within the specified time interval, get all policy states instead of the latest only.</span></span>

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

### <span data-ttu-id="8c8ee-178">-Apply</span><span class="sxs-lookup"><span data-stu-id="8c8ee-178">-Apply</span></span>
<span data-ttu-id="8c8ee-179">Применение выражения для агрегатов с помощью нотации OData.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-179">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="8c8ee-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c8ee-180">-DefaultProfile</span></span>
<span data-ttu-id="8c8ee-181">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-181">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c8ee-182">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="8c8ee-182">-Expand</span></span>
<span data-ttu-id="8c8ee-183">Расширение выражения с помощью нотации OData.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-183">Expand expression using OData notation.</span></span>

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

### <span data-ttu-id="8c8ee-184">-Filter</span><span class="sxs-lookup"><span data-stu-id="8c8ee-184">-Filter</span></span>
<span data-ttu-id="8c8ee-185">Фильтрация выражения с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-185">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="8c8ee-186">-From</span><span class="sxs-lookup"><span data-stu-id="8c8ee-186">-From</span></span>
<span data-ttu-id="8c8ee-187">Timestamp в формате ISO 8601, определяющий время начала интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-187">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="8c8ee-188">Если этот параметр не задан, по умолчанию значение параметра "To" за вычетом 1 дня.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-188">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="8c8ee-189">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8c8ee-189">-ManagementGroupName</span></span>
<span data-ttu-id="8c8ee-190">Имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-190">Management group name.</span></span>

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

### <span data-ttu-id="8c8ee-191">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="8c8ee-191">-OrderBy</span></span>
<span data-ttu-id="8c8ee-192">Выражение порядка с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-192">Ordering expression using OData notation.</span></span>
<span data-ttu-id="8c8ee-193">Одно или несколько имен столбцов, разделенных запятой, с необязательными именами "desc" (по умолчанию) или "asc".</span><span class="sxs-lookup"><span data-stu-id="8c8ee-193">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="8c8ee-194">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="8c8ee-194">-PolicyAssignmentName</span></span>
<span data-ttu-id="8c8ee-195">Имя назначения политики.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-195">Policy assignment name.</span></span>

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

### <span data-ttu-id="8c8ee-196">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8c8ee-196">-PolicyDefinitionName</span></span>
<span data-ttu-id="8c8ee-197">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-197">Policy definition name.</span></span>

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

### <span data-ttu-id="8c8ee-198">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8c8ee-198">-PolicySetDefinitionName</span></span>
<span data-ttu-id="8c8ee-199">Имя определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-199">Policy set definition name.</span></span>

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

### <span data-ttu-id="8c8ee-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c8ee-200">-ResourceGroupName</span></span>
<span data-ttu-id="8c8ee-201">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-201">Resource group name.</span></span>

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

### <span data-ttu-id="8c8ee-202">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c8ee-202">-ResourceId</span></span>
<span data-ttu-id="8c8ee-203">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-203">Resource ID.</span></span>

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

### <span data-ttu-id="8c8ee-204">-Select</span><span class="sxs-lookup"><span data-stu-id="8c8ee-204">-Select</span></span>
<span data-ttu-id="8c8ee-205">Выберите выражение, используя нотацию OData.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-205">Select expression using OData notation.</span></span>
<span data-ttu-id="8c8ee-206">Одно или несколько имен столбцов, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-206">One or more comma-separated column names.</span></span>
<span data-ttu-id="8c8ee-207">Ограничивает столбцы в каждой записи только теми, которые запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-207">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="8c8ee-208">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c8ee-208">-SubscriptionId</span></span>
<span data-ttu-id="8c8ee-209">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-209">Subscription ID.</span></span>

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

### <span data-ttu-id="8c8ee-210">-To</span><span class="sxs-lookup"><span data-stu-id="8c8ee-210">-To</span></span>
<span data-ttu-id="8c8ee-211">Timestamp в формате ISO 8601, определяющий время окончания интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-211">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="8c8ee-212">По умолчанию заданы значения времени запроса.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-212">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="8c8ee-213">-Top</span><span class="sxs-lookup"><span data-stu-id="8c8ee-213">-Top</span></span>
<span data-ttu-id="8c8ee-214">Максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-214">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="8c8ee-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8ee-215">CommonParameters</span></span>
<span data-ttu-id="8c8ee-216">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c8ee-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c8ee-217">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c8ee-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8ee-218">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c8ee-218">INPUTS</span></span>

### <span data-ttu-id="8c8ee-219">System.String</span><span class="sxs-lookup"><span data-stu-id="8c8ee-219">System.String</span></span>

## <span data-ttu-id="8c8ee-220">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c8ee-220">OUTPUTS</span></span>

### <span data-ttu-id="8c8ee-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span><span class="sxs-lookup"><span data-stu-id="8c8ee-221">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyState</span></span>

## <span data-ttu-id="8c8ee-222">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c8ee-222">NOTES</span></span>

## <span data-ttu-id="8c8ee-223">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c8ee-223">RELATED LINKS</span></span>

[<span data-ttu-id="8c8ee-224">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="8c8ee-224">Get-AzPolicyStateSummary</span></span>](./Get-AzPolicyStateSummary.md)
