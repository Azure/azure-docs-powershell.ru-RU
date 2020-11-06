---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
ms.openlocfilehash: e69ad25800dbf6aada7111a1093b4c878f3c0f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567700"
---
# <span data-ttu-id="59d36-101">Get-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="59d36-101">Get-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="59d36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59d36-102">SYNOPSIS</span></span>
<span data-ttu-id="59d36-103">Получение исправлений политики.</span><span class="sxs-lookup"><span data-stu-id="59d36-103">Gets policy remediations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59d36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59d36-104">SYNTAX</span></span>

### <span data-ttu-id="59d36-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59d36-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59d36-106">ByName</span><span class="sxs-lookup"><span data-stu-id="59d36-106">ByName</span></span>
```
Get-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59d36-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="59d36-107">GenericScope</span></span>
```
Get-AzureRmPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59d36-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="59d36-108">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59d36-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="59d36-109">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59d36-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59d36-110">ByResourceId</span></span>
```
Get-AzureRmPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59d36-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d36-111">DESCRIPTION</span></span>
<span data-ttu-id="59d36-112">Командлет **Get-AzureRmPolicyRemediation** получает все исправления политик в области или конкретное исправление.</span><span class="sxs-lookup"><span data-stu-id="59d36-112">The **Get-AzureRmPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="59d36-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59d36-113">EXAMPLES</span></span>

### <span data-ttu-id="59d36-114">Пример 1: получение всех исправлений политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="59d36-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Get-AzureRmPolicyRemediation
```

<span data-ttu-id="59d36-115">Эта команда получает все исправления, созданные в рамках подписки с именем "Моя подписка" или под ней.</span><span class="sxs-lookup"><span data-stu-id="59d36-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="59d36-116">Пример 2: получение конкретных исправлений политики и сведений о развертывании</span><span class="sxs-lookup"><span data-stu-id="59d36-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="59d36-117">Эта команда получает исправление с именем "remediation1" из группы ресурсов "myResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="59d36-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="59d36-118">Будут включены сведения о исправлении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59d36-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="59d36-119">Пример 3: получение 10 исправлений политики в группе "Управление" с дополнительными фильтрами</span><span class="sxs-lookup"><span data-stu-id="59d36-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="59d36-120">Эта команда получает из группы управления с именем "MG1" максимум 10 политик исправлений.</span><span class="sxs-lookup"><span data-stu-id="59d36-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="59d36-121">Будут извлекаться только исправления политик для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="59d36-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="59d36-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59d36-122">PARAMETERS</span></span>

### <span data-ttu-id="59d36-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d36-123">-DefaultProfile</span></span>
<span data-ttu-id="59d36-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59d36-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59d36-125">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="59d36-125">-Filter</span></span>
<span data-ttu-id="59d36-126">Выражение фильтра с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="59d36-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="59d36-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="59d36-127">-IncludeDetail</span></span>
<span data-ttu-id="59d36-128">Включите сведения о развертываниях, созданных функцией "исправление".</span><span class="sxs-lookup"><span data-stu-id="59d36-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="59d36-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="59d36-129">-ManagementGroupName</span></span>
<span data-ttu-id="59d36-130">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="59d36-130">Management group ID.</span></span>

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

### <span data-ttu-id="59d36-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59d36-131">-Name</span></span>
<span data-ttu-id="59d36-132">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="59d36-132">Resource name.</span></span>

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

### <span data-ttu-id="59d36-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d36-133">-ResourceGroupName</span></span>
<span data-ttu-id="59d36-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59d36-134">Resource group name.</span></span>

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

### <span data-ttu-id="59d36-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59d36-135">-ResourceId</span></span>
<span data-ttu-id="59d36-136">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="59d36-136">Resource ID.</span></span>

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

### <span data-ttu-id="59d36-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="59d36-137">-Scope</span></span>
<span data-ttu-id="59d36-138">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="59d36-138">Scope of the resource.</span></span> <span data-ttu-id="59d36-139">Например, "/subscriptions/{subscriptionId}/resourceGroups/{rgName}".</span><span class="sxs-lookup"><span data-stu-id="59d36-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="59d36-140">-Top</span><span class="sxs-lookup"><span data-stu-id="59d36-140">-Top</span></span>
<span data-ttu-id="59d36-141">Максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="59d36-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="59d36-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d36-142">CommonParameters</span></span>
<span data-ttu-id="59d36-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59d36-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d36-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d36-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d36-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59d36-145">INPUTS</span></span>

### <span data-ttu-id="59d36-146">System. String</span><span class="sxs-lookup"><span data-stu-id="59d36-146">System.String</span></span>

## <span data-ttu-id="59d36-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59d36-147">OUTPUTS</span></span>

### <span data-ttu-id="59d36-148">Microsoft. Azure. Commands. PolicyInsights. Models. unисправление. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="59d36-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="59d36-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="59d36-149">NOTES</span></span>

## <span data-ttu-id="59d36-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59d36-150">RELATED LINKS</span></span>
