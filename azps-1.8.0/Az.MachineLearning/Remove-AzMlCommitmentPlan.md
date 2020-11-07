---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 1c022d8ae97ac9f1e51bbabaff15a9dec61f5d87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899742"
---
# <span data-ttu-id="a8f04-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a8f04-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="a8f04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8f04-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f04-103">Удаление плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="a8f04-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="a8f04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8f04-104">SYNTAX</span></span>

### <span data-ttu-id="a8f04-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a8f04-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8f04-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a8f04-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8f04-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8f04-107">DESCRIPTION</span></span>
<span data-ttu-id="a8f04-108">Удаление плана фиксации машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="a8f04-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="a8f04-109">Обратите внимание, что планы обязательства, в которых есть связи обязательства, нельзя удалить.</span><span class="sxs-lookup"><span data-stu-id="a8f04-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="a8f04-110">Ассоциации обязательства можно удалить только по целевому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a8f04-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="a8f04-111">Например, если вы удалите веб-службу машинного обучения Azure, она также будет удалена, так как связь по обязательствам, связывающая веб-службу с планом фиксации.</span><span class="sxs-lookup"><span data-stu-id="a8f04-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="a8f04-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8f04-112">EXAMPLES</span></span>

### <span data-ttu-id="a8f04-113">Пример 1: Удаление плана обязательства</span><span class="sxs-lookup"><span data-stu-id="a8f04-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="a8f04-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8f04-114">PARAMETERS</span></span>

### <span data-ttu-id="a8f04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f04-115">-DefaultProfile</span></span>
<span data-ttu-id="a8f04-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a8f04-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8f04-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a8f04-117">-Force</span></span>
<span data-ttu-id="a8f04-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a8f04-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a8f04-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a8f04-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="a8f04-120">Объект веб-службы машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="a8f04-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f04-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a8f04-121">-Name</span></span>
<span data-ttu-id="a8f04-122">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a8f04-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f04-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f04-123">-ResourceGroupName</span></span>
<span data-ttu-id="a8f04-124">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="a8f04-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8f04-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8f04-125">-Confirm</span></span>
<span data-ttu-id="a8f04-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a8f04-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8f04-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8f04-127">-WhatIf</span></span>
<span data-ttu-id="a8f04-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a8f04-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8f04-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a8f04-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8f04-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f04-130">CommonParameters</span></span>
<span data-ttu-id="a8f04-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8f04-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f04-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8f04-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f04-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8f04-133">INPUTS</span></span>

### <span data-ttu-id="a8f04-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="a8f04-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="a8f04-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8f04-135">OUTPUTS</span></span>

### <span data-ttu-id="a8f04-136">System. void</span><span class="sxs-lookup"><span data-stu-id="a8f04-136">System.Void</span></span>

## <span data-ttu-id="a8f04-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8f04-137">NOTES</span></span>
<span data-ttu-id="a8f04-138">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="a8f04-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="a8f04-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8f04-139">RELATED LINKS</span></span>
