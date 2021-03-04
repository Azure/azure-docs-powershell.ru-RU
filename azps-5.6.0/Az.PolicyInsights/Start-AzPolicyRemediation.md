---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: aeb86609e06417147f5ef4600c430665f28da454
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989064"
---
# <span data-ttu-id="17e00-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="17e00-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="17e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17e00-102">SYNOPSIS</span></span>
<span data-ttu-id="17e00-103">Создает и запускает исправление политики для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="17e00-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="17e00-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="17e00-104">SYNTAX</span></span>

### <span data-ttu-id="17e00-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17e00-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e00-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="17e00-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17e00-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17e00-107">DESCRIPTION</span></span>
<span data-ttu-id="17e00-108">Для определенного назначения политики создается исправление политики с его началом- **AzPolicyRemediation.**</span><span class="sxs-lookup"><span data-stu-id="17e00-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="17e00-109">Все невыгодные ресурсы в области исправлений или ниже нее будут исправлены.</span><span class="sxs-lookup"><span data-stu-id="17e00-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="17e00-110">Исправление поддерживается только для политик с эффектом deployIfNotExists.</span><span class="sxs-lookup"><span data-stu-id="17e00-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="17e00-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="17e00-111">EXAMPLES</span></span>

### <span data-ttu-id="17e00-112">Пример 1. Запуск исправлений в области действия подписки</span><span class="sxs-lookup"><span data-stu-id="17e00-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="17e00-113">Эта команда создает новую исправление политики в подписке "Моя подписка" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="17e00-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="17e00-114">Пример 2. Запуск исправлений в области группы управления с помощью необязательных фильтров</span><span class="sxs-lookup"><span data-stu-id="17e00-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="17e00-115">Эта команда создает новую исправление политики в группе управления "mg1" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="17e00-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="17e00-116">Будут исправлены только ресурсы из западного или восточного регионов.</span><span class="sxs-lookup"><span data-stu-id="17e00-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="17e00-117">Пример 3. Запуск исправлений в области группировки ресурсов для назначения определения набора политик</span><span class="sxs-lookup"><span data-stu-id="17e00-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="17e00-118">Эта команда создает новую политику исправлений в группе ресурсов myRG для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="17e00-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="17e00-119">Назначение политики назначает определение набора политики (также называется инициативой).</span><span class="sxs-lookup"><span data-stu-id="17e00-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="17e00-120">Он указывает, какая политика внутри инициативы должна быть исправлена.</span><span class="sxs-lookup"><span data-stu-id="17e00-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="17e00-121">Пример 4. Запуск исправлений и ожидание завершения в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="17e00-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="17e00-122">Эта команда запускает новое исправление политики в подписке "Моя подписка" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="17e00-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="17e00-123">Перед возвратом последнего состояния исправлений исправление будет завершено.</span><span class="sxs-lookup"><span data-stu-id="17e00-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="17e00-124">Пример 5. Запуск исправлений, которые будут обнаруживать не соответствующими ресурсами, перед исправлением</span><span class="sxs-lookup"><span data-stu-id="17e00-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="17e00-125">Эта команда создает новую исправление политики в подписке "Моя подписка" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="17e00-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="17e00-126">Состояние соответствия ресурсов в подписке будет переоценно с соответствием назначению политики, а не соответствующим ресурсам будут исправлены.</span><span class="sxs-lookup"><span data-stu-id="17e00-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="17e00-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17e00-127">PARAMETERS</span></span>

### <span data-ttu-id="17e00-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17e00-128">-AsJob</span></span>
<span data-ttu-id="17e00-129">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="17e00-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="17e00-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e00-130">-DefaultProfile</span></span>
<span data-ttu-id="17e00-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17e00-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17e00-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="17e00-132">-LocationFilter</span></span>
<span data-ttu-id="17e00-133">Расположения ресурсов, которые должны быть включены в исправление.</span><span class="sxs-lookup"><span data-stu-id="17e00-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="17e00-134">Ресурсы, которые не находятся в этих расположениях, не будут исправлены.</span><span class="sxs-lookup"><span data-stu-id="17e00-134">Resources that don't reside in these locations will not be remediated.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e00-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="17e00-135">-ManagementGroupName</span></span>
<span data-ttu-id="17e00-136">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="17e00-136">Management group ID.</span></span>

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

### <span data-ttu-id="17e00-137">-Name</span><span class="sxs-lookup"><span data-stu-id="17e00-137">-Name</span></span>
<span data-ttu-id="17e00-138">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="17e00-138">Resource name.</span></span>

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

### <span data-ttu-id="17e00-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="17e00-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="17e00-140">ИД назначения политики.</span><span class="sxs-lookup"><span data-stu-id="17e00-140">Policy assignment ID.</span></span>
<span data-ttu-id="17e00-141">Например,</span><span class="sxs-lookup"><span data-stu-id="17e00-141">E.g.</span></span>
<span data-ttu-id="17e00-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="17e00-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e00-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="17e00-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="17e00-144">Возвращает номер ссылки определения политики на исправленное определение отдельного определения.</span><span class="sxs-lookup"><span data-stu-id="17e00-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="17e00-145">Требуется, когда назначению политики назначается определение набора политики.</span><span class="sxs-lookup"><span data-stu-id="17e00-145">Required when the policy assignment assigns a policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e00-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="17e00-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="17e00-147">В нем описывается, как в задаче по исправлению будут обнаружены ресурсы, которые необходимо от исправление.</span><span class="sxs-lookup"><span data-stu-id="17e00-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="17e00-148">ReEvaluateCompliance не поддерживается при исправлении областей групп управления.</span><span class="sxs-lookup"><span data-stu-id="17e00-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ExistingNonCompliant, ReEvaluateCompliance

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e00-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17e00-149">-ResourceGroupName</span></span>
<span data-ttu-id="17e00-150">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17e00-150">Resource group name.</span></span>

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

### <span data-ttu-id="17e00-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17e00-151">-ResourceId</span></span>
<span data-ttu-id="17e00-152">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="17e00-152">Resource ID.</span></span>

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

### <span data-ttu-id="17e00-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="17e00-153">-Scope</span></span>
<span data-ttu-id="17e00-154">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="17e00-154">Scope of the resource.</span></span>
<span data-ttu-id="17e00-155">Например,</span><span class="sxs-lookup"><span data-stu-id="17e00-155">E.g.</span></span>
<span data-ttu-id="17e00-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="17e00-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="17e00-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17e00-157">-Confirm</span></span>
<span data-ttu-id="17e00-158">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="17e00-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e00-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e00-159">-WhatIf</span></span>
<span data-ttu-id="17e00-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17e00-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e00-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="17e00-161">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e00-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e00-162">CommonParameters</span></span>
<span data-ttu-id="17e00-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17e00-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e00-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17e00-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e00-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17e00-165">INPUTS</span></span>

### <span data-ttu-id="17e00-166">System.String</span><span class="sxs-lookup"><span data-stu-id="17e00-166">System.String</span></span>

### <span data-ttu-id="17e00-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="17e00-167">System.String[]</span></span>

## <span data-ttu-id="17e00-168">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17e00-168">OUTPUTS</span></span>

### <span data-ttu-id="17e00-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="17e00-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="17e00-170">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="17e00-170">NOTES</span></span>

## <span data-ttu-id="17e00-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17e00-171">RELATED LINKS</span></span>
