---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyStateSummary.md
ms.openlocfilehash: ad622662615e74908c3d34c513e8570286b76297
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519797"
---
# <span data-ttu-id="565e9-101">Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="565e9-101">Get-AzPolicyStateSummary</span></span>

## <span data-ttu-id="565e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="565e9-102">SYNOPSIS</span></span>
<span data-ttu-id="565e9-103">Возвращает сводку по последним состояниям соответствия политике для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="565e9-103">Gets latest policy compliance states summary for resources.</span></span>

## <span data-ttu-id="565e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="565e9-104">SYNTAX</span></span>

### <span data-ttu-id="565e9-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="565e9-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="565e9-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="565e9-106">ManagementGroupScope</span></span>
```
Get-AzPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="565e9-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="565e9-107">ResourceGroupScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="565e9-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="565e9-108">PolicySetDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="565e9-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="565e9-109">PolicyDefinitionScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="565e9-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="565e9-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="565e9-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="565e9-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="565e9-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="565e9-112">ResourceScope</span></span>
```
Get-AzPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="565e9-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="565e9-113">DESCRIPTION</span></span>
<span data-ttu-id="565e9-114">Представление сводки номеров последних политик соответствия требованиям в различных областях, разбитое на назначения политик и определения политик.</span><span class="sxs-lookup"><span data-stu-id="565e9-114">Gets a summary view of latest policy compliance state numbers at various scopes, broken down into policy assignments and policy definitions.</span></span> <span data-ttu-id="565e9-115">Он включает только состояния, не совместимые с политиками.</span><span class="sxs-lookup"><span data-stu-id="565e9-115">It includes only non-compliant policy states.</span></span>

## <span data-ttu-id="565e9-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="565e9-116">EXAMPLES</span></span>

### <span data-ttu-id="565e9-117">Пример 1. Просмотр последних отчетов о состояниях политики, не соответствующим требованиям, в текущей области действия подписки</span><span class="sxs-lookup"><span data-stu-id="565e9-117">Example 1: Get latest non-compliant policy states summary in current subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary
```

<span data-ttu-id="565e9-118">Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="565e9-118">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="565e9-119">Пример 2. Вывод последних отчетов о состояниях, не совместимых с политиками, в указанной области подписки</span><span class="sxs-lookup"><span data-stu-id="565e9-119">Example 2: Get latest non-compliant policy states summary in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="565e9-120">Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="565e9-120">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="565e9-121">Пример 3. Получать последние сведения о состояниях политики, не соответствующим требованиям, в области группы управления</span><span class="sxs-lookup"><span data-stu-id="565e9-121">Example 3: Get latest non-compliant policy states summary in management group scope</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="565e9-122">Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="565e9-122">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="565e9-123">Пример 4. Получать последние сведения о состояниях политики, не соответствующим требованиям, в области группы ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="565e9-123">Example 4: Get latest non-compliant policy states summary in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="565e9-124">Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов в указанной группе ресурсов (в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="565e9-124">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="565e9-125">Пример 5. Получать последние сведения о состояниях политики, не соответствующим требованиям, в области группы ресурсов в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="565e9-125">Example 5: Get latest non-compliant policy states summary in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="565e9-126">Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="565e9-126">Gets the summary view of latest policy compliance states generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="565e9-127">Пример 6. Просмотр последних отчетов о состояниях, не совместимых с политиками, для ресурса</span><span class="sxs-lookup"><span data-stu-id="565e9-127">Example 6: Get latest non-compliant policy states summary for a resource</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="565e9-128">Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="565e9-128">Gets the summary view of latest policy compliance states generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="565e9-129">Пример 7. Просмотр последних отчетов о состояниях, не совместимых с политиками, для определения набора политик в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="565e9-129">Example 7: Get latest non-compliant policy states summary for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="565e9-130">Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное определение набора политики (которое существует в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="565e9-130">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="565e9-131">Пример 8. Просмотр последних отчетов о состояниях, не совместимых с политиками, для определения набора политик в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="565e9-131">Example 8: Get latest non-compliant policy states summary for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="565e9-132">Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в пределах клиента в текущем сеансе), на которые влияет указанное определение набора политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="565e9-132">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="565e9-133">Пример 9. Просмотр последних отчетов о состояниях, не совместимых с политиками, для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="565e9-133">Example 9: Get latest non-compliant policy states summary for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="565e9-134">Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в клиенте в контексте текущего сеанса), на которые влияет указанное определение политики (которое существует в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="565e9-134">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="565e9-135">Пример 10. Просмотр последних отчетов о состояниях, не совместимых с политиками, для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="565e9-135">Example 10: Get latest non-compliant policy states summary for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="565e9-136">Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в клиенте в контексте текущего сеанса), на которые влияет указанное определение политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="565e9-136">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="565e9-137">Пример 11. Просмотр последних отчетов о состояниях, не совместимых с политиками, для назначения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="565e9-137">Example 11: Get latest non-compliant policy states summary for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="565e9-138">Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в клиенте в текущем контексте сеанса), на которые влияет указанное назначение политики (которое существует в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="565e9-138">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="565e9-139">Пример 12. Просмотр последних отчетов о состояниях, не совместимых с политиками, для назначения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="565e9-139">Example 12: Get latest non-compliant policy states summary for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="565e9-140">Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в пределах клиента в контексте текущего сеанса), на которые влияет указанное назначение политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="565e9-140">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="565e9-141">Пример 13. Просмотр последних отчетов о состояниях, не совместимых с политиками, для назначения политики в указанной группе ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="565e9-141">Example 13: Get latest non-compliant policy states summary for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="565e9-142">Возвращает сводку по последним состояниям соответствия политике, созданным в последний день для всех ресурсов (в клиенте в текущем контексте сеанса), к влияниям указанного назначения политики (которое существует в группе ресурсов в подписке в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="565e9-142">Gets the summary view of latest policy compliance states generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="565e9-143">Пример 14. Просмотр последних отчетов о состояниях, не совместимых с политиками, в текущей области действия подписки с параметром "Верхний запрос"</span><span class="sxs-lookup"><span data-stu-id="565e9-143">Example 14: Get latest non-compliant policy states summary in current subscription scope, with Top query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Top 5
```

<span data-ttu-id="565e9-144">Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="565e9-144">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="565e9-145">Команда заказывает сводки назначений политики в результатах в порядке убываний не соответствующими требованиям ресурсами и выводит только 5 из них.</span><span class="sxs-lookup"><span data-stu-id="565e9-145">The command orders the policy assignment summaries in the results by non-compliant resource counts in descending order, and takes only top 5 of those policy assignment summaries.</span></span>

### <span data-ttu-id="565e9-146">Пример 15. Просмотр последних отчетов о состояниях политики, не соответствующим требованиям, в текущей области действия подписки с вариантами запросов "От" и "На"</span><span class="sxs-lookup"><span data-stu-id="565e9-146">Example 15: Get latest non-compliant policy states summary in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="565e9-147">Возвращает сводку по последним состояниям соответствия политике, созданную в диапазоне дат, указанном для всех ресурсов подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="565e9-147">Gets the summary view of latest policy compliance states generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="565e9-148">Пример 16. Просмотр последних отчетов о состояниях политики, не соответствующим требованиям, в текущей области действия подписки с параметром "Фильтровать запрос"</span><span class="sxs-lookup"><span data-stu-id="565e9-148">Example 16: Get latest non-compliant policy states summary in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="565e9-149">Возвращает сводку по последним состояниям соответствия политике, созданную в последний день для всех ресурсов подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="565e9-149">Gets the summary view of latest policy compliance states generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="565e9-150">Команда ограничивает результаты, возвращаемые с помощью фильтрации на основе действия определения политики (включая действия запрета или аудита) и расположения ресурсов (за исключением расположения на востоке).</span><span class="sxs-lookup"><span data-stu-id="565e9-150">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions), and resource location (excludes eastus location).</span></span>

## <span data-ttu-id="565e9-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="565e9-151">PARAMETERS</span></span>

### <span data-ttu-id="565e9-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565e9-152">-DefaultProfile</span></span>
<span data-ttu-id="565e9-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="565e9-153">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="565e9-154">-Filter</span><span class="sxs-lookup"><span data-stu-id="565e9-154">-Filter</span></span>
<span data-ttu-id="565e9-155">Фильтрация выражения с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="565e9-155">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="565e9-156">-From</span><span class="sxs-lookup"><span data-stu-id="565e9-156">-From</span></span>
<span data-ttu-id="565e9-157">Timestamp в формате ISO 8601, определяющий время начала интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="565e9-157">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="565e9-158">Если этот параметр не задан, по умолчанию значение параметра "To" за вычетом 1 дня.</span><span class="sxs-lookup"><span data-stu-id="565e9-158">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

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

### <span data-ttu-id="565e9-159">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="565e9-159">-ManagementGroupName</span></span>
<span data-ttu-id="565e9-160">Имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="565e9-160">Management group name.</span></span>

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

### <span data-ttu-id="565e9-161">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="565e9-161">-PolicyAssignmentName</span></span>
<span data-ttu-id="565e9-162">Имя назначения политики.</span><span class="sxs-lookup"><span data-stu-id="565e9-162">Policy assignment name.</span></span>

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

### <span data-ttu-id="565e9-163">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="565e9-163">-PolicyDefinitionName</span></span>
<span data-ttu-id="565e9-164">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="565e9-164">Policy definition name.</span></span>

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

### <span data-ttu-id="565e9-165">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="565e9-165">-PolicySetDefinitionName</span></span>
<span data-ttu-id="565e9-166">Имя определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="565e9-166">Policy set definition name.</span></span>

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

### <span data-ttu-id="565e9-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="565e9-167">-ResourceGroupName</span></span>
<span data-ttu-id="565e9-168">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="565e9-168">Resource group name.</span></span>

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

### <span data-ttu-id="565e9-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="565e9-169">-ResourceId</span></span>
<span data-ttu-id="565e9-170">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="565e9-170">Resource ID.</span></span>

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

### <span data-ttu-id="565e9-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="565e9-171">-SubscriptionId</span></span>
<span data-ttu-id="565e9-172">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="565e9-172">Subscription ID.</span></span>

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

### <span data-ttu-id="565e9-173">-To</span><span class="sxs-lookup"><span data-stu-id="565e9-173">-To</span></span>
<span data-ttu-id="565e9-174">Timestamp в формате ISO 8601, определяющий время окончания интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="565e9-174">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="565e9-175">По умолчанию заданы значения времени запроса.</span><span class="sxs-lookup"><span data-stu-id="565e9-175">When not specified, defaults to time of request.</span></span>

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

### <span data-ttu-id="565e9-176">-Top</span><span class="sxs-lookup"><span data-stu-id="565e9-176">-Top</span></span>
<span data-ttu-id="565e9-177">Максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="565e9-177">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="565e9-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565e9-178">CommonParameters</span></span>
<span data-ttu-id="565e9-179">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="565e9-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565e9-180">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="565e9-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565e9-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="565e9-181">INPUTS</span></span>

### <span data-ttu-id="565e9-182">System.String</span><span class="sxs-lookup"><span data-stu-id="565e9-182">System.String</span></span>

## <span data-ttu-id="565e9-183">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="565e9-183">OUTPUTS</span></span>

### <span data-ttu-id="565e9-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="565e9-184">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyStateSummary</span></span>

## <span data-ttu-id="565e9-185">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="565e9-185">NOTES</span></span>

## <span data-ttu-id="565e9-186">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="565e9-186">RELATED LINKS</span></span>

[<span data-ttu-id="565e9-187">Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="565e9-187">Get-AzPolicyState</span></span>](./Get-AzPolicyState.md)
