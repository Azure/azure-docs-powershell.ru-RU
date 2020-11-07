---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: 93c31a9a8a1b2f161553efdabce2d97ed19caacd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729825"
---
# <span data-ttu-id="a04c8-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="a04c8-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="a04c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a04c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a04c8-103">Получает актуальные сведения о состояниях соответствия политике для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a04c8-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="a04c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a04c8-104">SYNTAX</span></span>

### <span data-ttu-id="a04c8-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a04c8-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a04c8-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="a04c8-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a04c8-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="a04c8-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a04c8-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="a04c8-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a04c8-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="a04c8-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a04c8-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="a04c8-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a04c8-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="a04c8-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a04c8-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="a04c8-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a04c8-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a04c8-113">DESCRIPTION</span></span>
<span data-ttu-id="a04c8-114">Возвращает представление сводки о последних параметрах соответствия политике в различных областях, с разбивкой на назначения политики и определения политик.</span><span class="sxs-lookup"><span data-stu-id="a04c8-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="a04c8-115">Она содержит только несоответствующие состояния политики.</span><span class="sxs-lookup"><span data-stu-id="a04c8-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="a04c8-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a04c8-116">EXAMPLES</span></span>

### <span data-ttu-id="a04c8-117">Пример 1: получение последних несоответствующих состояний политики сводка в текущей области подписки</span><span class="sxs-lookup"><span data-stu-id="a04c8-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="a04c8-118">Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="a04c8-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="a04c8-119">Пример 2: получение актуальной сводки о состояниях политик, не соответствующих требованиям, в указанной области действия подписки</span><span class="sxs-lookup"><span data-stu-id="a04c8-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="a04c8-120">Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="a04c8-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="a04c8-121">Пример 3: получение последних несовместимых состояний политики в области группы управления</span><span class="sxs-lookup"><span data-stu-id="a04c8-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="a04c8-122">Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="a04c8-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="a04c8-123">Пример 4: получение последних несовместимых состояний политики в области "область группы ресурсов" в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="a04c8-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="a04c8-124">Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в указанной группе ресурсов (в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="a04c8-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="a04c8-125">Пример 5: получение последних несоответствующих состояний политики в области "область группы ресурсов" в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="a04c8-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="a04c8-126">Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="a04c8-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="a04c8-127">Пример 6: получение последних несовместимых состояний политики для ресурса</span><span class="sxs-lookup"><span data-stu-id="a04c8-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="a04c8-128">Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="a04c8-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="a04c8-129">Пример 7: получение последних несовместимых состояний политики для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="a04c8-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="a04c8-130">Возвращает представление сводки о последних политиках соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением набора политик (которое существует в подписке в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="a04c8-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="a04c8-131">Пример 8: получение последних несовместимых состояний политики для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="a04c8-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="a04c8-132">Возвращает представление сводки о последних политиках соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением набора политик (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="a04c8-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="a04c8-133">Пример 9: получение последних несовместимых состояний политики для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="a04c8-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="a04c8-134">Возвращает представление сводки о последних политиках соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="a04c8-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="a04c8-135">Пример 10: получение последних несовместимых состояний политики для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="a04c8-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="a04c8-136">Возвращает представление сводки о последних политиках соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="a04c8-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="a04c8-137">Пример 11: получение последних несовместимых состояний политики для назначения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="a04c8-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="a04c8-138">Возвращает представление сводки о последних политиках соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (оно существует в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="a04c8-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="a04c8-139">Пример 12: получение последних несовместимых состояний политики для назначения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="a04c8-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="a04c8-140">Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="a04c8-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="a04c8-141">Пример 13: получение последних несовместимых состояний политики для назначения политики в указанной группе ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="a04c8-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="a04c8-142">Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в группе ресурсов в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="a04c8-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="a04c8-143">Пример 14: получение последних несоответствующих состояний политики в текущей области подписки с параметром Top Query</span><span class="sxs-lookup"><span data-stu-id="a04c8-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="a04c8-144">Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="a04c8-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="a04c8-145">Команда упорядочивает данные о назначениях политики в результатах по убывающему представлению несоответствующих ресурсов в порядке убывания и использует только первые 5 из этих сводок назначений политики.</span><span class="sxs-lookup"><span data-stu-id="a04c8-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="a04c8-146">Пример 15: получение последних несоответствующих состояний политики в текущей области подписки с параметрами "из" и "по запросу"</span><span class="sxs-lookup"><span data-stu-id="a04c8-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="a04c8-147">Возвращает представление сводки о последних состояниях соответствия политике, созданных в диапазоне дат, указанном для всех ресурсов в контексте текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="a04c8-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="a04c8-148">Пример 16: получение последних несоответствующих состояний политики в текущей области подписки с помощью параметра "запрос фильтра"</span><span class="sxs-lookup"><span data-stu-id="a04c8-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="a04c8-149">Возвращает представление сводки о последних состояниях соответствия политике, созданных за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="a04c8-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="a04c8-150">Команда ограничивает результаты, возвращаемые фильтром, на основе действия с определением политики (в том числе действия запрета или аудита) и расположения ресурсов (исключение расположения eastus).</span><span class="sxs-lookup"><span data-stu-id="a04c8-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="a04c8-151">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a04c8-151">PARAMETERS</span></span>

### <span data-ttu-id="a04c8-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04c8-152">-DefaultProfile</span></span>
<span data-ttu-id="a04c8-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a04c8-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a04c8-154">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="a04c8-154">-Filter</span></span>
<span data-ttu-id="a04c8-155">Выражение фильтра с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="a04c8-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="a04c8-156">-From</span><span class="sxs-lookup"><span data-stu-id="a04c8-156">-From</span></span>
<span data-ttu-id="a04c8-157">Отформатированная отметка времени ISO 8601 с указанием времени начала интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="a04c8-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="a04c8-158">Если не указано, по умолчанию используется значение параметра "до" за вычетом 1 дня.</span><span class="sxs-lookup"><span data-stu-id="a04c8-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="a04c8-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a04c8-159">-ManagementGroupName</span></span>
<span data-ttu-id="a04c8-160">Имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="a04c8-160">Management group name.</span></span>

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

### <span data-ttu-id="a04c8-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="a04c8-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="a04c8-162">Имя назначения политики.</span><span class="sxs-lookup"><span data-stu-id="a04c8-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="a04c8-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a04c8-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="a04c8-164">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="a04c8-164">Policy definition name.</span></span>

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

### <span data-ttu-id="a04c8-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a04c8-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="a04c8-166">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="a04c8-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="a04c8-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a04c8-167">-ResourceGroupName</span></span>
<span data-ttu-id="a04c8-168">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a04c8-168">Resource group name.</span></span>

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

### <span data-ttu-id="a04c8-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a04c8-169">-ResourceId</span></span>
<span data-ttu-id="a04c8-170">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a04c8-170">Resource ID.</span></span>

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

### <span data-ttu-id="a04c8-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a04c8-171">-SubscriptionId</span></span>
<span data-ttu-id="a04c8-172">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="a04c8-172">Subscription ID.</span></span>

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

### <span data-ttu-id="a04c8-173">-To</span><span class="sxs-lookup"><span data-stu-id="a04c8-173">-To</span></span>
<span data-ttu-id="a04c8-174">Отформатированная отметка времени ISO 8601, указывающая время окончания интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="a04c8-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="a04c8-175">Если не указано, по умолчанию используется время запроса.</span><span class="sxs-lookup"><span data-stu-id="a04c8-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="a04c8-176">-Top</span><span class="sxs-lookup"><span data-stu-id="a04c8-176">-Top</span></span>
<span data-ttu-id="a04c8-177">Максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="a04c8-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="a04c8-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04c8-178">CommonParameters</span></span>
<span data-ttu-id="a04c8-179">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a04c8-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04c8-180">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a04c8-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04c8-181">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a04c8-181">INPUTS</span></span>

### <span data-ttu-id="a04c8-182">System. String</span><span class="sxs-lookup"><span data-stu-id="a04c8-182">System.String</span></span>

## <span data-ttu-id="a04c8-183">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a04c8-183">OUTPUTS</span></span>

### <span data-ttu-id="a04c8-184">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="a04c8-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="a04c8-185">Пуск</span><span class="sxs-lookup"><span data-stu-id="a04c8-185">NOTES</span></span>

## <span data-ttu-id="a04c8-186">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a04c8-186">RELATED LINKS</span></span>

[<span data-ttu-id="a04c8-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="a04c8-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
