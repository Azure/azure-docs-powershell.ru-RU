---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44c12e08ca66c19cf3541f4abb200e1ba0663208
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505452"
---
# <span data-ttu-id="2d4da-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="2d4da-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="2d4da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d4da-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4da-103">Возвращает исправление политики.</span><span class="sxs-lookup"><span data-stu-id="2d4da-103">Gets policy remediations.</span></span>

## <span data-ttu-id="2d4da-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d4da-104">SYNTAX</span></span>

### <span data-ttu-id="2d4da-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d4da-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d4da-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2d4da-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d4da-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="2d4da-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d4da-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="2d4da-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d4da-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="2d4da-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d4da-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2d4da-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d4da-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d4da-111">DESCRIPTION</span></span>
<span data-ttu-id="2d4da-112">Для **получения всех исправлений** политики в области или в определенном исправлении с еготем вы получаете все изменения политики.</span><span class="sxs-lookup"><span data-stu-id="2d4da-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="2d4da-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d4da-113">EXAMPLES</span></span>

### <span data-ttu-id="2d4da-114">Пример 1. Все меры политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="2d4da-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="2d4da-115">Эта команда получает все меры, созданные в подписке "Моя подписка" или под ней.</span><span class="sxs-lookup"><span data-stu-id="2d4da-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="2d4da-116">Пример 2. Получите сведения об определенном исправлении политики и развертывании</span><span class="sxs-lookup"><span data-stu-id="2d4da-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="2d4da-117">Эта команда получает исправление с именем "исправление1" из группы ресурсов "myResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="2d4da-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="2d4da-118">Будут включены сведения о том, что ресурсы будут исправлены.</span><span class="sxs-lookup"><span data-stu-id="2d4da-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="2d4da-119">Пример 3. Получите 10 исправлений политики в группе управления с необязательными фильтрами</span><span class="sxs-lookup"><span data-stu-id="2d4da-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="2d4da-120">Эта команда получает не более 10 исправлений политики из группы управления "mg1".</span><span class="sxs-lookup"><span data-stu-id="2d4da-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="2d4da-121">Будут восстановлены только меры политики для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="2d4da-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="2d4da-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d4da-122">PARAMETERS</span></span>

### <span data-ttu-id="2d4da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4da-123">-DefaultProfile</span></span>
<span data-ttu-id="2d4da-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d4da-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d4da-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="2d4da-125">-Filter</span></span>
<span data-ttu-id="2d4da-126">Фильтрация выражения с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="2d4da-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="2d4da-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="2d4da-127">-IncludeDetail</span></span>
<span data-ttu-id="2d4da-128">Укаймь подробные сведения о развертываниях, созданных в исправлении.</span><span class="sxs-lookup"><span data-stu-id="2d4da-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="2d4da-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="2d4da-129">-ManagementGroupName</span></span>
<span data-ttu-id="2d4da-130">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="2d4da-130">Management group ID.</span></span>

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

### <span data-ttu-id="2d4da-131">-Name</span><span class="sxs-lookup"><span data-stu-id="2d4da-131">-Name</span></span>
<span data-ttu-id="2d4da-132">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d4da-132">Resource name.</span></span>

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

### <span data-ttu-id="2d4da-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d4da-133">-ResourceGroupName</span></span>
<span data-ttu-id="2d4da-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d4da-134">Resource group name.</span></span>

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

### <span data-ttu-id="2d4da-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d4da-135">-ResourceId</span></span>
<span data-ttu-id="2d4da-136">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d4da-136">Resource ID.</span></span>

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

### <span data-ttu-id="2d4da-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="2d4da-137">-Scope</span></span>
<span data-ttu-id="2d4da-138">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d4da-138">Scope of the resource.</span></span> <span data-ttu-id="2d4da-139">Например: '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="2d4da-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="2d4da-140">-Top</span><span class="sxs-lookup"><span data-stu-id="2d4da-140">-Top</span></span>
<span data-ttu-id="2d4da-141">Максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="2d4da-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="2d4da-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4da-142">CommonParameters</span></span>
<span data-ttu-id="2d4da-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4da-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4da-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d4da-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4da-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d4da-145">INPUTS</span></span>

### <span data-ttu-id="2d4da-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2d4da-146">System.String</span></span>

## <span data-ttu-id="2d4da-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d4da-147">OUTPUTS</span></span>

### <span data-ttu-id="2d4da-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="2d4da-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="2d4da-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d4da-149">NOTES</span></span>

## <span data-ttu-id="2d4da-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d4da-150">RELATED LINKS</span></span>
