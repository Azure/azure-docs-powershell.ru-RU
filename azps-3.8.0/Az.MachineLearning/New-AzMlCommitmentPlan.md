---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: 7d3d65e10864848cb1564b7137321c911c153ce0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074242"
---
# <span data-ttu-id="32024-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="32024-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="32024-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32024-102">SYNOPSIS</span></span>
<span data-ttu-id="32024-103">Создание нового плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="32024-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="32024-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32024-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32024-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32024-105">DESCRIPTION</span></span>
<span data-ttu-id="32024-106">Создание плана фиксации машинного обучения Azure в существующей группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32024-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="32024-107">Если в группе ресурсов есть план обязательства с таким же именем, этот звонок действует как операция обновления, и существующий план обязательства перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="32024-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="32024-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32024-108">EXAMPLES</span></span>

### <span data-ttu-id="32024-109">Пример 1: создание нового плана обязательства</span><span class="sxs-lookup"><span data-stu-id="32024-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="32024-110">Создание нового плана фиксации машинного обучения Azure с именем "MyCommitmentPlanName" в группе "MyResourceGroup" и в Южной Центральной области США.</span><span class="sxs-lookup"><span data-stu-id="32024-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="32024-111">В этом примере используется SKU DevTest/Standard, что означает, что ресурсы, предоставляемые планом обязательства, будут определяться ограничениями DevTest/Standard.</span><span class="sxs-lookup"><span data-stu-id="32024-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="32024-112">SkuCapacity в этом примере — это 1, что означает, что стоимость плана будет изменяться стоимостью DevTest, а ресурсы, содержащиеся в плане, будут изменяться в расчете на 1x, на которых DevTest предоставляется.</span><span class="sxs-lookup"><span data-stu-id="32024-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="32024-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32024-113">PARAMETERS</span></span>

### <span data-ttu-id="32024-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32024-114">-DefaultProfile</span></span>
<span data-ttu-id="32024-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="32024-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32024-116">-Force</span><span class="sxs-lookup"><span data-stu-id="32024-116">-Force</span></span>
<span data-ttu-id="32024-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="32024-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="32024-118">-Location</span><span class="sxs-lookup"><span data-stu-id="32024-118">-Location</span></span>
<span data-ttu-id="32024-119">Расположение плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="32024-119">The location of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32024-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32024-120">-Name</span></span>
<span data-ttu-id="32024-121">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="32024-121">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32024-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32024-122">-ResourceGroupName</span></span>
<span data-ttu-id="32024-123">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="32024-123">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32024-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="32024-124">-SkuCapacity</span></span>
<span data-ttu-id="32024-125">Емкость SKU, используемая при подготовке плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="32024-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="32024-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="32024-126">-SkuName</span></span>
<span data-ttu-id="32024-127">Имя SKU, которое будет использоваться при подготовке плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="32024-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32024-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="32024-128">-SkuTier</span></span>
<span data-ttu-id="32024-129">Уровень SKU, который будет использоваться при подготовке плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="32024-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32024-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32024-130">-Confirm</span></span>
<span data-ttu-id="32024-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32024-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32024-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32024-132">-WhatIf</span></span>
<span data-ttu-id="32024-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32024-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32024-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32024-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32024-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32024-135">CommonParameters</span></span>
<span data-ttu-id="32024-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32024-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32024-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32024-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32024-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32024-138">INPUTS</span></span>

### <span data-ttu-id="32024-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="32024-139">None</span></span>

## <span data-ttu-id="32024-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32024-140">OUTPUTS</span></span>

### <span data-ttu-id="32024-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="32024-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="32024-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="32024-142">NOTES</span></span>
<span data-ttu-id="32024-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="32024-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="32024-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32024-144">RELATED LINKS</span></span>
