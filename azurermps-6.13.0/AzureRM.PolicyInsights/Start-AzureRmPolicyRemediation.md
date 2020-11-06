---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/start-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Start-AzureRmPolicyRemediation.md
ms.openlocfilehash: d5a0d4cd14f86c782defd7b70a1edee209982d2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560784"
---
# <span data-ttu-id="d4e3e-101">Start-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="d4e3e-101">Start-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="d4e3e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e3e-103">Создание и запуск исправления политики для назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-103">Creates and starts a policy remediation for a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4e3e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4e3e-104">SYNTAX</span></span>

### <span data-ttu-id="d4e3e-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4e3e-105">ByName (Default)</span></span>
```
Start-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] -PolicyAssignmentId <String> [-PolicyDefinitionReferenceId <String>]
 [-LocationFilter <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4e3e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d4e3e-106">ByResourceId</span></span>
```
Start-AzureRmPolicyRemediation -ResourceId <String> -PolicyAssignmentId <String>
 [-PolicyDefinitionReferenceId <String>] [-LocationFilter <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e3e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4e3e-107">DESCRIPTION</span></span>
<span data-ttu-id="d4e3e-108">Командлет **Start-AzureRmPolicyRemediation** создает исправление политики для определенного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-108">The **Start-AzureRmPolicyRemediation** cmdlet creates a policy remediation for a particular policy assignment.</span></span> <span data-ttu-id="d4e3e-109">Все несоответствующие ресурсы на уровне или ниже области исправлений будут исправлены.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-109">All non-compliant resources at or below the remediation's scope will be remediated.</span></span> <span data-ttu-id="d4e3e-110">Исправление поддерживается только для политик с эффектом "deployIfNotExists".</span><span class="sxs-lookup"><span data-stu-id="d4e3e-110">Remediation is only supported for policies with the 'deployIfNotExists' effect.</span></span>

## <span data-ttu-id="d4e3e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4e3e-111">EXAMPLES</span></span>

### <span data-ttu-id="d4e3e-112">Пример 1: начало исправления в области подписки</span><span class="sxs-lookup"><span data-stu-id="d4e3e-112">Example 1: Start a remediation at subscription scope</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1"
```

<span data-ttu-id="d4e3e-113">Эта команда создает новое исправление политики в подписке "Моя подписка" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-113">This command creates a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span>

### <span data-ttu-id="d4e3e-114">Пример 2: начало исправления в области группы управления с необязательными фильтрами</span><span class="sxs-lookup"><span data-stu-id="d4e3e-114">Example 2: Start a remediation at management group scope with optional filters</span></span>
```
PS C:\> $policyAssignmentId = "/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1"
PS C:\> Start-AzureRmPolicyRemediation -ManagementGroupName "mg1" -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -LocationFilter "westus","eastus"
```

<span data-ttu-id="d4e3e-115">Эта команда создает новое исправление политики в группе управления "MG1" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-115">This command creates a new policy remediation in management group 'mg1' for the given policy assignment.</span></span> <span data-ttu-id="d4e3e-116">Будут исправлены только ресурсы из местоположений "westus" или "eastus".</span><span class="sxs-lookup"><span data-stu-id="d4e3e-116">Only resources in the 'westus' or 'eastus' locations will be remediated.</span></span>

### <span data-ttu-id="d4e3e-117">Пример 3: запуск исправления в области "Группа ресурсов" для задания определения политики</span><span class="sxs-lookup"><span data-stu-id="d4e3e-117">Example 3: Start a remediation at resource group scope for a policy set definition assignment</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/resourceGroups/myRG/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Start-AzureRmPolicyRemediation -ResourceGroupName "myRG" -PolicyAssignmentId $policyAssignmentId -PolicyDefinitionReferenceId "0349234412441" -Name "remediation1"
```

<span data-ttu-id="d4e3e-118">Эта команда создает новое исправление политики в группе ресурсов "myRG" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-118">This command creates a new policy remediation in resource group 'myRG' for the given policy assignment.</span></span> <span data-ttu-id="d4e3e-119">Назначение политики назначает определению набор политик (также называемое инициативой).</span><span class="sxs-lookup"><span data-stu-id="d4e3e-119">The policy assignment assigns a policy set definition (also known as an initiative).</span></span> <span data-ttu-id="d4e3e-120">Идентификатор ссылки определения политики указывает, какая политика в этой инициативе должна быть исправлена.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-120">The policy definition reference ID indicates which policy within the initiative should be remediated.</span></span>

### <span data-ttu-id="d4e3e-121">Пример 4: начните исправление и дождитесь завершения его работы в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-121">Example 4: Start a remediation and wait for it to complete in the background</span></span>
```
PS C:\> $policyAssignmentId = "/subscriptions/f0710c27-9663-4c05-19f8-1b4be01e86a5/providers/Microsoft.Authorization/policyAssignments/2deae24764b447c29af7c309"
PS C:\> Select-AzureRmSubscription -Subscription f0710c27-9663-4c05-19f8-1b4be01e86a5
PS C:\> $job = Start-AzureRmPolicyRemediation -PolicyAssignmentId $policyAssignmentId -Name "remediation1" -AsJob
PS C:\> $job | Wait-Job
PS C:\> $remediation = $job | Receive-Job
```

<span data-ttu-id="d4e3e-122">Эта команда запускает новое исправление политики в подписке "Моя подписка" для данного назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-122">This command starts a new policy remediation in subscription 'My Subscription' for the given policy assignment.</span></span> <span data-ttu-id="d4e3e-123">Перед возвращением финального состояния исправления оно будет ждать завершения исправления.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-123">It will wait for the remediation to complete before returning the final remediation status.</span></span>

## <span data-ttu-id="d4e3e-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4e3e-124">PARAMETERS</span></span>

### <span data-ttu-id="d4e3e-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4e3e-125">-AsJob</span></span>
<span data-ttu-id="d4e3e-126">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d4e3e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e3e-127">-DefaultProfile</span></span>
<span data-ttu-id="d4e3e-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e3e-129">-LocationFilter</span><span class="sxs-lookup"><span data-stu-id="d4e3e-129">-LocationFilter</span></span>
<span data-ttu-id="d4e3e-130">Расположения ресурсов, которые должны быть включены в исправление.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-130">The resource locations that should be included in the remediation.</span></span>
<span data-ttu-id="d4e3e-131">Ресурсы, не размещенные в этих расположениях, не будут исправлены.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-131">Resources that don't reside in these locations will not be remediated.</span></span>

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

### <span data-ttu-id="d4e3e-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e3e-132">-ManagementGroupName</span></span>
<span data-ttu-id="d4e3e-133">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-133">Management group ID.</span></span>

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

### <span data-ttu-id="d4e3e-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d4e3e-134">-Name</span></span>
<span data-ttu-id="d4e3e-135">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-135">Resource name.</span></span>

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

### <span data-ttu-id="d4e3e-136">-PolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="d4e3e-136">-PolicyAssignmentId</span></span>
<span data-ttu-id="d4e3e-137">Идентификатор назначения политики.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-137">Policy assignment ID.</span></span>
<span data-ttu-id="d4e3e-138">Сокращен.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-138">E.g.</span></span>
<span data-ttu-id="d4e3e-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-139">'/subscriptions/{subscriptionId}/providers/Microsoft.Authorization/policyAssignments/{assignmentName}'.</span></span>

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

### <span data-ttu-id="d4e3e-140">-PolicyDefinitionReferenceId</span><span class="sxs-lookup"><span data-stu-id="d4e3e-140">-PolicyDefinitionReferenceId</span></span>
<span data-ttu-id="d4e3e-141">Получает идентификатор ссылки на определение политики для отдельного определения, которое будет исправлено.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-141">Gets the policy definition reference ID of the individual definition that is being remediated.</span></span>
<span data-ttu-id="d4e3e-142">Обязательно, если назначение политики присваивает определению набор политик.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-142">Required when the policy assignment assigns a policy set definition.</span></span>

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

### <span data-ttu-id="d4e3e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e3e-143">-ResourceGroupName</span></span>
<span data-ttu-id="d4e3e-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-144">Resource group name.</span></span>

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

### <span data-ttu-id="d4e3e-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4e3e-145">-ResourceId</span></span>
<span data-ttu-id="d4e3e-146">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-146">Resource ID.</span></span>

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

### <span data-ttu-id="d4e3e-147">-Scope</span><span class="sxs-lookup"><span data-stu-id="d4e3e-147">-Scope</span></span>
<span data-ttu-id="d4e3e-148">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-148">Scope of the resource.</span></span>
<span data-ttu-id="d4e3e-149">Сокращен.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-149">E.g.</span></span>
<span data-ttu-id="d4e3e-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-150">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="d4e3e-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4e3e-151">-Confirm</span></span>
<span data-ttu-id="d4e3e-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e3e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e3e-153">-WhatIf</span></span>
<span data-ttu-id="d4e3e-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e3e-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e3e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e3e-156">CommonParameters</span></span>
<span data-ttu-id="d4e3e-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4e3e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e3e-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e3e-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e3e-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4e3e-159">INPUTS</span></span>

### <span data-ttu-id="d4e3e-160">System. String</span><span class="sxs-lookup"><span data-stu-id="d4e3e-160">System.String</span></span>

### <span data-ttu-id="d4e3e-161">System. String []</span><span class="sxs-lookup"><span data-stu-id="d4e3e-161">System.String[]</span></span>

## <span data-ttu-id="d4e3e-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4e3e-162">OUTPUTS</span></span>

### <span data-ttu-id="d4e3e-163">Microsoft. Azure. Commands. PolicyInsights. Models. unисправление. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="d4e3e-163">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="d4e3e-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4e3e-164">NOTES</span></span>

## <span data-ttu-id="d4e3e-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4e3e-165">RELATED LINKS</span></span>
