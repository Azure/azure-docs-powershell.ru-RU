---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 733f473ed09807c33355ac6bc22491a160e5481a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074226"
---
# <span data-ttu-id="ff5dd-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ff5dd-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="ff5dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff5dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5dd-103">Обновляет свойства существующего ресурса плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="ff5dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff5dd-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff5dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff5dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ff5dd-106">Обновляет существующий ресурс плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="ff5dd-107">Обратите внимание, что большая часть свойств плана обязательства является постоянной и не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="ff5dd-108">Свойства, которые можно изменить, включают SKU (с помощью которого можно перенести план обязательства из одного SKU в другой) и на теги.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="ff5dd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff5dd-109">EXAMPLES</span></span>

### <span data-ttu-id="ff5dd-110">Пример 1: Обновление плана обязательства</span><span class="sxs-lookup"><span data-stu-id="ff5dd-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="ff5dd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff5dd-111">PARAMETERS</span></span>

### <span data-ttu-id="ff5dd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5dd-112">-DefaultProfile</span></span>
<span data-ttu-id="ff5dd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ff5dd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff5dd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ff5dd-114">-Force</span></span>
<span data-ttu-id="ff5dd-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ff5dd-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff5dd-116">-Name</span></span>
<span data-ttu-id="ff5dd-117">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ff5dd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff5dd-118">-ResourceGroupName</span></span>
<span data-ttu-id="ff5dd-119">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ff5dd-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ff5dd-120">-SkuCapacity</span></span>
<span data-ttu-id="ff5dd-121">Емкость SKU, используемая при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ff5dd-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ff5dd-122">-SkuName</span></span>
<span data-ttu-id="ff5dd-123">Имя SKU, которое будет использоваться при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ff5dd-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ff5dd-124">-SkuTier</span></span>
<span data-ttu-id="ff5dd-125">Уровень SKU, который будет использоваться при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ff5dd-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="ff5dd-126">-Tag</span></span>
<span data-ttu-id="ff5dd-127">Теги для ресурса плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff5dd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff5dd-128">-Confirm</span></span>
<span data-ttu-id="ff5dd-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff5dd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff5dd-130">-WhatIf</span></span>
<span data-ttu-id="ff5dd-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff5dd-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff5dd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5dd-133">CommonParameters</span></span>
<span data-ttu-id="ff5dd-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff5dd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5dd-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5dd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5dd-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff5dd-136">INPUTS</span></span>

### <span data-ttu-id="ff5dd-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="ff5dd-137">None</span></span>

## <span data-ttu-id="ff5dd-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff5dd-138">OUTPUTS</span></span>

### <span data-ttu-id="ff5dd-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ff5dd-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="ff5dd-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff5dd-140">NOTES</span></span>
<span data-ttu-id="ff5dd-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ff5dd-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ff5dd-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff5dd-142">RELATED LINKS</span></span>
