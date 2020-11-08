---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyRemediation.md
ms.openlocfilehash: e4a0e3ad4ffac7e610f5807c7687cdc1bf548770
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246867"
---
# <span data-ttu-id="50796-101">Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="50796-101">Start-AzPolicyRemediation</span></span>

## <span data-ttu-id="50796-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50796-102">SYNOPSIS</span></span>
<span data-ttu-id="50796-103">Создание и запуск исправления политики для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="50796-103">Creates and starts a policy remediation for a policy assignment.</span></span>

## <span data-ttu-id="50796-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50796-104">SYNTAX</span></span>

### <span data-ttu-id="50796-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50796-105">ByName (Default)</span></span>
```
Start-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50796-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="50796-106">ByResourceId</span></span>
```
Start-AzPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-ResourceDiscoveryMode <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50796-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50796-107">DESCRIPTION</span></span>
<span data-ttu-id="50796-108">Командлет **Start-AzPolicyRemediation** создает исправление политики для определенного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="50796-108">The **Start-AzPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="50796-109">Все несоответствующие ресурсы на уровне или ниже области исправлений будут исправлены.</span><span class="sxs-lookup"><span data-stu-id="50796-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="50796-110">Исправление поддерживается только для политик с эффектом "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="50796-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="50796-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50796-111">EXAMPLES</span></span>

### <span data-ttu-id="50796-112">Пример 1: начало исправления в области подписки</span><span class="sxs-lookup"><span data-stu-id="50796-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="50796-113">Эта команда создает новое исправление политики в подписке "Моя подписка" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="50796-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="50796-114">Пример 2: начало исправления в области группы управления с необязательными фильтрами</span><span class="sxs-lookup"><span data-stu-id="50796-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="50796-115">Эта команда создает новое исправление политики в группе управления "MG1" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="50796-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="50796-116">Будут исправлены только ресурсы из местоположений "westus" или "eastus".</span><span class="sxs-lookup"><span data-stu-id="50796-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="50796-117">Пример 3: запуск исправления в области "Группа ресурсов" для задания определения политики</span><span class="sxs-lookup"><span data-stu-id="50796-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="50796-118">Эта команда создает новое исправление политики в группе ресурсов "myRG" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="50796-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="50796-119">Назначение политики назначает определению набор политик (также называемое инициативой).</span><span class="sxs-lookup"><span data-stu-id="50796-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="50796-120">Идентификатор ссылки определения политики указывает, какая политика в этой инициативе должна быть исправлена.</span><span class="sxs-lookup"><span data-stu-id="50796-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="50796-121">Пример 4: начните исправление и дождитесь завершения его работы в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="50796-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="50796-122">Эта команда запускает новое исправление политики в подписке "Моя подписка" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="50796-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="50796-123">Перед возвращением финального состояния исправления оно будет ждать завершения исправления.</span><span class="sxs-lookup"><span data-stu-id="50796-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

### <span data-ttu-id="50796-124">Пример 5: начните исправление, которое будет распознавать ресурсы, не соответствующие требованиям, перед исправление</span><span class="sxs-lookup"><span data-stu-id="50796-124">Example 5: Start a remediation that will discover non-compliant resources before remediating</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Start-AzPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -ResourceDiscoveryMode ReEvaluateCompliance
```

<span data-ttu-id="50796-125">Эта команда создает новое исправление политики в подписке "Моя подписка" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="50796-125">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="50796-126">Состояние соответствия ресурсов в подписке будет перечислено с учетом назначения политики и несоответствующих ресурсов будут исправлены.</span><span class="sxs-lookup"><span data-stu-id="50796-126">The compliance state of resources in the subscription will be re-evaluated against the policy assignment and non-compliant resources will be remediated.</span></span>

## <span data-ttu-id="50796-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50796-127">PARAMETERS</span></span>

### <span data-ttu-id="50796-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50796-128">-AsJob</span></span>
<span data-ttu-id="50796-129">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="50796-129">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="50796-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50796-130">-DefaultProfile</span></span>
<span data-ttu-id="50796-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50796-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50796-132">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="50796-132">-LocationFilter</span></span>
<span data-ttu-id="50796-133">Расположения ресурсов, которые должны быть включены в исправление.</span><span class="sxs-lookup"><span data-stu-id="50796-133">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="50796-134">Ресурсы, не размещенные в этих расположениях, не будут исправлены.</span><span class="sxs-lookup"><span data-stu-id="50796-134">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="50796-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="50796-135">-ManagementGroupName</span></span>
<span data-ttu-id="50796-136">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="50796-136">Management group ID.</span></span>

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

### <span data-ttu-id="50796-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="50796-137">-Name</span></span>
<span data-ttu-id="50796-138">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="50796-138">Resource name.</span></span>

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

### <span data-ttu-id="50796-139">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="50796-139">-PolicyAssignmentId</span></span>
<span data-ttu-id="50796-140">Идентификатор назначения политики.</span><span class="sxs-lookup"><span data-stu-id="50796-140">Policy assignment ID.</span></span>
<span data-ttu-id="50796-141">Сокращен.</span><span class="sxs-lookup"><span data-stu-id="50796-141">E.g.</span></span>
<span data-ttu-id="50796-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="50796-142">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="50796-143">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="50796-143">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="50796-144">Получает идентификатор ссылки на определение политики для отдельного определения, которое будет исправлено.</span><span class="sxs-lookup"><span data-stu-id="50796-144">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="50796-145">Обязательно, если назначение политики присваивает определению набор политик.</span><span class="sxs-lookup"><span data-stu-id="50796-145">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="50796-146">-ResourceDiscoveryMode</span><span class="sxs-lookup"><span data-stu-id="50796-146">-ResourceDiscoveryMode</span></span>
<span data-ttu-id="50796-147">В этой статье описано, как задача «исправление» обнаружит ресурсы, которые необходимо исправить.</span><span class="sxs-lookup"><span data-stu-id="50796-147">Describes how the remediation task will discover resources that need to be remediated.</span></span>
<span data-ttu-id="50796-148">ReEvaluateCompliance не поддерживается в областях групп управления исправление.</span><span class="sxs-lookup"><span data-stu-id="50796-148">ReEvaluateCompliance is not supported when remediating management group scopes.</span></span>

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

### <span data-ttu-id="50796-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50796-149">-ResourceGroupName</span></span>
<span data-ttu-id="50796-150">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50796-150">Resource group name.</span></span>

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

### <span data-ttu-id="50796-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50796-151">-ResourceId</span></span>
<span data-ttu-id="50796-152">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="50796-152">Resource ID.</span></span>

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

### <span data-ttu-id="50796-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="50796-153">-Scope</span></span>
<span data-ttu-id="50796-154">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="50796-154">Scope of the resource.</span></span>
<span data-ttu-id="50796-155">Сокращен.</span><span class="sxs-lookup"><span data-stu-id="50796-155">E.g.</span></span>
<span data-ttu-id="50796-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="50796-156">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="50796-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50796-157">-Confirm</span></span>
<span data-ttu-id="50796-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="50796-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50796-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50796-159">-WhatIf</span></span>
<span data-ttu-id="50796-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="50796-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50796-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="50796-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50796-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50796-162">CommonParameters</span></span>
<span data-ttu-id="50796-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50796-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50796-164">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50796-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50796-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50796-165">INPUTS</span></span>

### <span data-ttu-id="50796-166">System. String</span><span class="sxs-lookup"><span data-stu-id="50796-166">System.String</span></span>

### <span data-ttu-id="50796-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="50796-167">System.String[]</span></span>

## <span data-ttu-id="50796-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50796-168">OUTPUTS</span></span>

### <span data-ttu-id="50796-169">Microsoft. Azure. Commands. PolicyInsights. Models. unисправление. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="50796-169">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="50796-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="50796-170">NOTES</span></span>

## <span data-ttu-id="50796-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50796-171">RELATED LINKS</span></span>
