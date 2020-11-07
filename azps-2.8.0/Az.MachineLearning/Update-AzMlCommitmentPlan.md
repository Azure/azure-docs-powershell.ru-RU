---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: c1aa160d7a0773569255f425f3993de0b47d552a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720423"
---
# <span data-ttu-id="f31c9-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f31c9-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="f31c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f31c9-102">SYNOPSIS</span></span>
<span data-ttu-id="f31c9-103">Обновляет свойства существующего ресурса плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="f31c9-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="f31c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f31c9-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f31c9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f31c9-105">DESCRIPTION</span></span>
<span data-ttu-id="f31c9-106">Обновляет существующий ресурс плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="f31c9-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="f31c9-107">Обратите внимание, что большая часть свойств плана обязательства является постоянной и не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="f31c9-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="f31c9-108">Свойства, которые можно изменить, включают SKU (с помощью которого можно перенести план обязательства из одного SKU в другой) и на теги.</span><span class="sxs-lookup"><span data-stu-id="f31c9-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="f31c9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f31c9-109">EXAMPLES</span></span>

### <span data-ttu-id="f31c9-110">Пример 1: Обновление плана обязательства</span><span class="sxs-lookup"><span data-stu-id="f31c9-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="f31c9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f31c9-111">PARAMETERS</span></span>

### <span data-ttu-id="f31c9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31c9-112">-DefaultProfile</span></span>
<span data-ttu-id="f31c9-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f31c9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f31c9-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f31c9-114">-Force</span></span>
<span data-ttu-id="f31c9-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f31c9-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f31c9-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f31c9-116">-Name</span></span>
<span data-ttu-id="f31c9-117">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f31c9-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f31c9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f31c9-118">-ResourceGroupName</span></span>
<span data-ttu-id="f31c9-119">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f31c9-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f31c9-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f31c9-120">-SkuCapacity</span></span>
<span data-ttu-id="f31c9-121">Емкость SKU, используемая при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f31c9-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f31c9-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f31c9-122">-SkuName</span></span>
<span data-ttu-id="f31c9-123">Имя SKU, которое будет использоваться при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f31c9-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f31c9-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f31c9-124">-SkuTier</span></span>
<span data-ttu-id="f31c9-125">Уровень SKU, который будет использоваться при обновлении плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f31c9-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f31c9-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="f31c9-126">-Tag</span></span>
<span data-ttu-id="f31c9-127">Теги для ресурса плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="f31c9-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="f31c9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f31c9-128">-Confirm</span></span>
<span data-ttu-id="f31c9-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f31c9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f31c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f31c9-130">-WhatIf</span></span>
<span data-ttu-id="f31c9-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f31c9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f31c9-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f31c9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f31c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31c9-133">CommonParameters</span></span>
<span data-ttu-id="f31c9-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f31c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31c9-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f31c9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31c9-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f31c9-136">INPUTS</span></span>

### <span data-ttu-id="f31c9-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="f31c9-137">None</span></span>

## <span data-ttu-id="f31c9-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f31c9-138">OUTPUTS</span></span>

### <span data-ttu-id="f31c9-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f31c9-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="f31c9-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="f31c9-140">NOTES</span></span>
<span data-ttu-id="f31c9-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f31c9-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f31c9-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f31c9-142">RELATED LINKS</span></span>
