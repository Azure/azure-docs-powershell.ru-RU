---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: d2745a0dd73141c1da7d049494e3a1545ee92599
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568505"
---
# <span data-ttu-id="97bc7-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="97bc7-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="97bc7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="97bc7-103">Создание нового плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="97bc7-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97bc7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97bc7-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97bc7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="97bc7-106">Создание плана фиксации машинного обучения Azure в существующей группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97bc7-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="97bc7-107">Если в группе ресурсов есть план обязательства с таким же именем, этот звонок действует как операция обновления, и существующий план обязательства перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="97bc7-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="97bc7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97bc7-108">EXAMPLES</span></span>

### <span data-ttu-id="97bc7-109">Пример 1: создание нового плана обязательства</span><span class="sxs-lookup"><span data-stu-id="97bc7-109">Example 1: Create a new commitment plan</span></span>
```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="97bc7-110">Создание нового плана фиксации машинного обучения Azure с именем "MyCommitmentPlanName" в группе "MyResourceGroup" и в Южной Центральной области США.</span><span class="sxs-lookup"><span data-stu-id="97bc7-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="97bc7-111">В этом примере используется SKU DevTest/Standard, что означает, что ресурсы, предоставленные планом обязательства, будут definied на ограничения DevTest/Standard.</span><span class="sxs-lookup"><span data-stu-id="97bc7-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="97bc7-112">SkuCapacity в этом примере — это 1, что означает, что стоимость плана будет изменяться стоимостью DevTest, а ресурсы, содержащиеся в плане, будут изменяться в расчете на 1x, на которых DevTest предоставляется.</span><span class="sxs-lookup"><span data-stu-id="97bc7-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="97bc7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97bc7-113">PARAMETERS</span></span>

### <span data-ttu-id="97bc7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97bc7-114">-DefaultProfile</span></span>
<span data-ttu-id="97bc7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="97bc7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97bc7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="97bc7-116">-Force</span></span>
<span data-ttu-id="97bc7-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="97bc7-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="97bc7-118">-Location</span><span class="sxs-lookup"><span data-stu-id="97bc7-118">-Location</span></span>
<span data-ttu-id="97bc7-119">Расположение плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="97bc7-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="97bc7-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97bc7-120">-Name</span></span>
<span data-ttu-id="97bc7-121">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="97bc7-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="97bc7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97bc7-122">-ResourceGroupName</span></span>
<span data-ttu-id="97bc7-123">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="97bc7-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="97bc7-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="97bc7-124">-SkuCapacity</span></span>
<span data-ttu-id="97bc7-125">Емкость SKU, используемая при подготовке плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="97bc7-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="97bc7-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="97bc7-126">-SkuName</span></span>
<span data-ttu-id="97bc7-127">Имя SKU, которое будет использоваться при подготовке плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="97bc7-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="97bc7-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="97bc7-128">-SkuTier</span></span>
<span data-ttu-id="97bc7-129">Уровень SKU, который будет использоваться при подготовке плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="97bc7-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="97bc7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97bc7-130">-Confirm</span></span>
<span data-ttu-id="97bc7-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="97bc7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97bc7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97bc7-132">-WhatIf</span></span>
<span data-ttu-id="97bc7-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="97bc7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97bc7-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="97bc7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97bc7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97bc7-135">CommonParameters</span></span>
<span data-ttu-id="97bc7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97bc7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97bc7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97bc7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97bc7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97bc7-138">INPUTS</span></span>

### <span data-ttu-id="97bc7-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="97bc7-139">None</span></span>

## <span data-ttu-id="97bc7-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97bc7-140">OUTPUTS</span></span>

### <span data-ttu-id="97bc7-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="97bc7-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="97bc7-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="97bc7-142">NOTES</span></span>
<span data-ttu-id="97bc7-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="97bc7-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="97bc7-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97bc7-144">RELATED LINKS</span></span>
