---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 744618bb2cc12b4d57bfb1ed42267fcbbe7a86ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505454"
---
# <span data-ttu-id="16c3e-101">Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="16c3e-101">Get-AzPolicyEvent</span></span>

## <span data-ttu-id="16c3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="16c3e-103">Возвращает события оценки политики, созданные по мере создания или обновления ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16c3e-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

## <span data-ttu-id="16c3e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="16c3e-104">SYNTAX</span></span>

### <span data-ttu-id="16c3e-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16c3e-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c3e-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="16c3e-106">ManagementGroupScope</span></span>
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c3e-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="16c3e-107">ResourceGroupScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c3e-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="16c3e-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c3e-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="16c3e-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c3e-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="16c3e-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c3e-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="16c3e-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16c3e-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="16c3e-112">ResourceScope</span></span>
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16c3e-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16c3e-113">DESCRIPTION</span></span>
<span data-ttu-id="16c3e-114">Возвращает события оценки политики, созданные по мере создания или обновления ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16c3e-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="16c3e-115">Записи событий политики можно запрашивать в различных областях на основе заданного интервала времени (по умолчанию — последний день).</span><span class="sxs-lookup"><span data-stu-id="16c3e-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="16c3e-116">Результаты можно вычислять с фильтрацией, группировкой и групповыми агрегатами.</span><span class="sxs-lookup"><span data-stu-id="16c3e-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="16c3e-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="16c3e-117">EXAMPLES</span></span>

### <span data-ttu-id="16c3e-118">Пример 1. Просмотр событий политики в текущей области подписки</span><span class="sxs-lookup"><span data-stu-id="16c3e-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent
```

<span data-ttu-id="16c3e-119">Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="16c3e-120">Пример 2. Просмотр событий политики в указанной области подписки</span><span class="sxs-lookup"><span data-stu-id="16c3e-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="16c3e-121">Возвращает записи событий политики, созданные в последний день для всех ресурсов в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="16c3e-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="16c3e-122">Пример 3. Просмотр событий политики в области группы управления</span><span class="sxs-lookup"><span data-stu-id="16c3e-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="16c3e-123">Возвращает записи событий политики, созданные в последний день для всех ресурсов в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="16c3e-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="16c3e-124">Пример 4. Получать события политики в области группы ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="16c3e-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="16c3e-125">Возвращает записи событий политики, созданные в последний день для всех ресурсов в указанной группе ресурсов (в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="16c3e-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="16c3e-126">Пример 5. Получать события политики в области группы ресурсов в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="16c3e-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="16c3e-127">Возвращает записи событий политики, созданные в последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="16c3e-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="16c3e-128">Пример 6. Получить события политики для ресурса</span><span class="sxs-lookup"><span data-stu-id="16c3e-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="16c3e-129">Возвращает записи событий политики, созданные в последний день для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="16c3e-130">Пример 7. Просмотр событий политики для определения набора политик в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="16c3e-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="16c3e-131">Получает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное определение набора политики (которое существует в подписке в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="16c3e-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="16c3e-132">Пример 8. Получить события политики для определения набора политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="16c3e-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="16c3e-133">Возвращает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное определение набора политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="16c3e-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="16c3e-134">Пример 9. Получить события политики для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="16c3e-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="16c3e-135">Получает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное определение политики (которое существует в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="16c3e-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="16c3e-136">Пример 10. Получить события политики для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="16c3e-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="16c3e-137">Возвращает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное определение политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="16c3e-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="16c3e-138">Пример 11. Просмотр событий политики для назначения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="16c3e-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="16c3e-139">Возвращает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), к работе с помощью указанного назначения политики (которое существует в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="16c3e-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="16c3e-140">Пример 12. Получить события политики для назначения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="16c3e-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="16c3e-141">Возвращает записи событий политики, созданные в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное назначение политики (существующее в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="16c3e-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="16c3e-142">Пример 13. Получить события политики для назначения политики в указанной группе ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="16c3e-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="16c3e-143">Возвращает записи событий политики, созданные в последний день для всех ресурсов (в клиенте в текущем контексте сеанса), к работе с помощью указанного назначения политики (которое существует в группе ресурсов в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="16c3e-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="16c3e-144">Пример 14. Просмотр событий политики в текущей области подписки с вариантами запроса OrderBy, Top и Select</span><span class="sxs-lookup"><span data-stu-id="16c3e-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="16c3e-145">Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="16c3e-146">Эта команда отбирает результаты по свойствам timestamp и policy assignment (Имя назначения политики) и отбирает только 5 из 5 перечислены в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="16c3e-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="16c3e-147">Кроме того, для каждой записи будет выбрано только подмножество столбцов.</span><span class="sxs-lookup"><span data-stu-id="16c3e-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="16c3e-148">Пример 15. Просмотр событий политики в текущей области подписки с вариантами запросов "От" и "На"</span><span class="sxs-lookup"><span data-stu-id="16c3e-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="16c3e-149">Возвращает записи событий политики, созданные в диапазоне дат, указанном для всех ресурсов подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="16c3e-150">Пример 16. Просмотр событий политики в текущей области подписки с параметром "Фильтровать запрос"</span><span class="sxs-lookup"><span data-stu-id="16c3e-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="16c3e-151">Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="16c3e-152">Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая действия запрета или аудита) и расположения ресурсов (за исключением расположения на востоке).</span><span class="sxs-lookup"><span data-stu-id="16c3e-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="16c3e-153">Пример 17. Получение событий политики в текущей области подписки с указанием агрегата "Применить" для подсчета строк</span><span class="sxs-lookup"><span data-stu-id="16c3e-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="16c3e-154">Возвращает количество записей событий политики, созданных в последний день для всех ресурсов подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="16c3e-155">Команда возвращает количество только записей событий политики, которое возвращается в свойстве AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="16c3e-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="16c3e-156">Пример 18. Получение событий политики в текущей области подписки с указанием группировки с агрегатом "Применить"</span><span class="sxs-lookup"><span data-stu-id="16c3e-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="16c3e-157">Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="16c3e-158">Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая только события аудита и запрета).</span><span class="sxs-lookup"><span data-stu-id="16c3e-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="16c3e-159">Она группирует результаты на основе назначения политики, определения политики, действия определения политики и ид ресурса, а также вычисляет количество записей в каждой группе, возвращаемой в свойстве AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="16c3e-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="16c3e-160">Она упорядочена по результатам подсчета в порядке убывления и занимает только 5 лучших из перечислены в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="16c3e-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="16c3e-161">Пример 19. Получение событий политики в текущей области подписки с указанием группировки без агрегирования</span><span class="sxs-lookup"><span data-stu-id="16c3e-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="16c3e-162">Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="16c3e-163">Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая только события аудита и запрета).</span><span class="sxs-lookup"><span data-stu-id="16c3e-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="16c3e-164">Результаты группируются на основе ид ресурса. Будет создан список всех ресурсов в подписке, которые создали событие политики как минимум для одной политики аудита или запрета.</span><span class="sxs-lookup"><span data-stu-id="16c3e-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="16c3e-165">Пример 20. Получение событий политики в текущей области действия подписки с указанием нескольких групп</span><span class="sxs-lookup"><span data-stu-id="16c3e-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="16c3e-166">Возвращает записи событий политики, созданные в последний день для всех ресурсов в рамках подписки в контексте текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="16c3e-167">Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая только события запрета).</span><span class="sxs-lookup"><span data-stu-id="16c3e-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="16c3e-168">Сначала результаты группируются на основе назначения политики, определения политики и ид ресурса. Затем она затем группирует результаты этой группировки с такими же свойствами, за исключением ид ресурса, и вычисляет количество записей в каждой из этих групп, возвращаемого в свойстве AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="16c3e-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="16c3e-169">Она упорядочена по результатам подсчета в порядке убывления и занимает только 5 лучших из перечислены в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="16c3e-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="16c3e-170">При этом создаются 5 самых распространенных политик запрета с большим количеством отказано в ресурсах.</span><span class="sxs-lookup"><span data-stu-id="16c3e-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="16c3e-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16c3e-171">PARAMETERS</span></span>

### <span data-ttu-id="16c3e-172">-Apply</span><span class="sxs-lookup"><span data-stu-id="16c3e-172">-Apply</span></span>
<span data-ttu-id="16c3e-173">Применение выражения для агрегатов с помощью нотации OData.</span><span class="sxs-lookup"><span data-stu-id="16c3e-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="16c3e-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c3e-174">-DefaultProfile</span></span>
<span data-ttu-id="16c3e-175">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16c3e-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c3e-176">-Filter</span><span class="sxs-lookup"><span data-stu-id="16c3e-176">-Filter</span></span>
<span data-ttu-id="16c3e-177">Фильтрация выражения с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="16c3e-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="16c3e-178">-From</span><span class="sxs-lookup"><span data-stu-id="16c3e-178">-From</span></span>
<span data-ttu-id="16c3e-179">Timestamp в формате ISO 8601, определяющий время начала интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="16c3e-180">Если этот параметр не задан, по умолчанию значение параметра "To" за вычетом 1 дня.</span><span class="sxs-lookup"><span data-stu-id="16c3e-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="16c3e-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="16c3e-181">-ManagementGroupName</span></span>
<span data-ttu-id="16c3e-182">Имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="16c3e-182">Management group name.</span></span>

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

### <span data-ttu-id="16c3e-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="16c3e-183">-OrderBy</span></span>
<span data-ttu-id="16c3e-184">Выражение порядка с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="16c3e-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="16c3e-185">Одно или несколько имен столбцов, разделенных запятой, с необязательными именами "desc" (по умолчанию) или "asc".</span><span class="sxs-lookup"><span data-stu-id="16c3e-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="16c3e-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="16c3e-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="16c3e-187">Имя назначения политики.</span><span class="sxs-lookup"><span data-stu-id="16c3e-187">Policy assignment name.</span></span>

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

### <span data-ttu-id="16c3e-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="16c3e-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="16c3e-189">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="16c3e-189">Policy definition name.</span></span>

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

### <span data-ttu-id="16c3e-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="16c3e-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="16c3e-191">Имя определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="16c3e-191">Policy set definition name.</span></span>

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

### <span data-ttu-id="16c3e-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c3e-192">-ResourceGroupName</span></span>
<span data-ttu-id="16c3e-193">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16c3e-193">Resource group name.</span></span>

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

### <span data-ttu-id="16c3e-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16c3e-194">-ResourceId</span></span>
<span data-ttu-id="16c3e-195">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-195">Resource ID.</span></span>

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

### <span data-ttu-id="16c3e-196">-Select</span><span class="sxs-lookup"><span data-stu-id="16c3e-196">-Select</span></span>
<span data-ttu-id="16c3e-197">Выберите выражение, используя нотацию OData.</span><span class="sxs-lookup"><span data-stu-id="16c3e-197">Select expression using OData notation.</span></span>
<span data-ttu-id="16c3e-198">Одно или несколько имен столбцов, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="16c3e-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="16c3e-199">Ограничивает столбцы в каждой записи только теми, которые запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="16c3e-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="16c3e-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16c3e-200">-SubscriptionId</span></span>
<span data-ttu-id="16c3e-201">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="16c3e-201">Subscription ID.</span></span>

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

### <span data-ttu-id="16c3e-202">-To</span><span class="sxs-lookup"><span data-stu-id="16c3e-202">-To</span></span>
<span data-ttu-id="16c3e-203">Timestamp в формате ISO 8601, определяющий время окончания интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="16c3e-204">По умолчанию заданы значения времени запроса.</span><span class="sxs-lookup"><span data-stu-id="16c3e-204">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="16c3e-205">-Top</span><span class="sxs-lookup"><span data-stu-id="16c3e-205">-Top</span></span>
<span data-ttu-id="16c3e-206">Максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="16c3e-206">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="16c3e-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c3e-207">CommonParameters</span></span>
<span data-ttu-id="16c3e-208">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c3e-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c3e-209">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16c3e-209">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c3e-210">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16c3e-210">INPUTS</span></span>

### <span data-ttu-id="16c3e-211">System.String</span><span class="sxs-lookup"><span data-stu-id="16c3e-211">System.String</span></span>

## <span data-ttu-id="16c3e-212">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16c3e-212">OUTPUTS</span></span>

### <span data-ttu-id="16c3e-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="16c3e-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="16c3e-214">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="16c3e-214">NOTES</span></span>

## <span data-ttu-id="16c3e-215">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16c3e-215">RELATED LINKS</span></span>
