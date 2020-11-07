---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44f7d3331d32092636c53850b0315f34b7df7808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904553"
---
# <span data-ttu-id="01a13-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="01a13-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="01a13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01a13-102">SYNOPSIS</span></span>
<span data-ttu-id="01a13-103">Получение исправлений политики.</span><span class="sxs-lookup"><span data-stu-id="01a13-103">Gets policy remediations.</span></span>

## <span data-ttu-id="01a13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01a13-104">SYNTAX</span></span>

### <span data-ttu-id="01a13-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01a13-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01a13-106">ByName</span><span class="sxs-lookup"><span data-stu-id="01a13-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01a13-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="01a13-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01a13-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="01a13-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01a13-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="01a13-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01a13-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="01a13-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01a13-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01a13-111">DESCRIPTION</span></span>
<span data-ttu-id="01a13-112">Командлет **Get-AzPolicyRemediation** получает все исправления политик в области или конкретное исправление.</span><span class="sxs-lookup"><span data-stu-id="01a13-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="01a13-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01a13-113">EXAMPLES</span></span>

### <span data-ttu-id="01a13-114">Пример 1: получение всех исправлений политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="01a13-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="01a13-115">Эта команда получает все исправления, созданные в рамках подписки с именем "Моя подписка" или под ней.</span><span class="sxs-lookup"><span data-stu-id="01a13-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="01a13-116">Пример 2: получение конкретных исправлений политики и сведений о развертывании</span><span class="sxs-lookup"><span data-stu-id="01a13-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="01a13-117">Эта команда получает исправление с именем "remediation1" из группы ресурсов "myResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="01a13-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="01a13-118">Будут включены сведения о исправлении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01a13-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="01a13-119">Пример 3: получение 10 исправлений политики в группе "Управление" с дополнительными фильтрами</span><span class="sxs-lookup"><span data-stu-id="01a13-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="01a13-120">Эта команда получает из группы управления с именем "MG1" максимум 10 политик исправлений.</span><span class="sxs-lookup"><span data-stu-id="01a13-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="01a13-121">Будут извлекаться только исправления политик для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="01a13-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="01a13-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01a13-122">PARAMETERS</span></span>

### <span data-ttu-id="01a13-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a13-123">-DefaultProfile</span></span>
<span data-ttu-id="01a13-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01a13-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01a13-125">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="01a13-125">-Filter</span></span>
<span data-ttu-id="01a13-126">Выражение фильтра с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="01a13-126">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, GenericScope, ManagementGroupScope, ResourceGroupScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a13-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="01a13-127">-IncludeDetail</span></span>
<span data-ttu-id="01a13-128">Включите сведения о развертываниях, созданных функцией "исправление".</span><span class="sxs-lookup"><span data-stu-id="01a13-128">Include details of the deployments created by the remediation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a13-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="01a13-129">-ManagementGroupName</span></span>
<span data-ttu-id="01a13-130">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="01a13-130">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="01a13-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01a13-131">-Name</span></span>
<span data-ttu-id="01a13-132">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="01a13-132">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a13-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a13-133">-ResourceGroupName</span></span>
<span data-ttu-id="01a13-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01a13-134">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a13-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01a13-135">-ResourceId</span></span>
<span data-ttu-id="01a13-136">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="01a13-136">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a13-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="01a13-137">-Scope</span></span>
<span data-ttu-id="01a13-138">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="01a13-138">Scope of the resource.</span></span> <span data-ttu-id="01a13-139">Например, "/subscriptions/{subscriptionId}/resourceGroups/{rgName}".</span><span class="sxs-lookup"><span data-stu-id="01a13-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GenericScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a13-140">-Top</span><span class="sxs-lookup"><span data-stu-id="01a13-140">-Top</span></span>
<span data-ttu-id="01a13-141">Максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="01a13-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="01a13-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a13-142">CommonParameters</span></span>
<span data-ttu-id="01a13-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01a13-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a13-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a13-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a13-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01a13-145">INPUTS</span></span>

### <span data-ttu-id="01a13-146">System. String</span><span class="sxs-lookup"><span data-stu-id="01a13-146">System.String</span></span>

## <span data-ttu-id="01a13-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01a13-147">OUTPUTS</span></span>

### <span data-ttu-id="01a13-148">Microsoft. Azure. Commands. PolicyInsights. Models. unисправление. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="01a13-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="01a13-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="01a13-149">NOTES</span></span>

## <span data-ttu-id="01a13-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01a13-150">RELATED LINKS</span></span>
