---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 8593853817739438176b70424ab529f0811d90de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248925"
---
# <span data-ttu-id="d29b4-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d29b4-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="d29b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d29b4-102">SYNOPSIS</span></span>
<span data-ttu-id="d29b4-103">Удаление плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="d29b4-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="d29b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d29b4-104">SYNTAX</span></span>

### <span data-ttu-id="d29b4-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d29b4-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d29b4-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="d29b4-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d29b4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d29b4-107">DESCRIPTION</span></span>
<span data-ttu-id="d29b4-108">Удаление плана фиксации машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="d29b4-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="d29b4-109">Обратите внимание, что планы обязательства, в которых есть связи обязательства, нельзя удалить.</span><span class="sxs-lookup"><span data-stu-id="d29b4-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="d29b4-110">Ассоциации обязательства можно удалить только по целевому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="d29b4-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="d29b4-111">Например, если вы удалите веб-службу машинного обучения Azure, она также будет удалена, так как связь по обязательствам, связывающая веб-службу с планом фиксации.</span><span class="sxs-lookup"><span data-stu-id="d29b4-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="d29b4-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d29b4-112">EXAMPLES</span></span>

### <span data-ttu-id="d29b4-113">Пример 1: Удаление плана обязательства</span><span class="sxs-lookup"><span data-stu-id="d29b4-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="d29b4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d29b4-114">PARAMETERS</span></span>

### <span data-ttu-id="d29b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d29b4-115">-DefaultProfile</span></span>
<span data-ttu-id="d29b4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d29b4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d29b4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d29b4-117">-Force</span></span>
<span data-ttu-id="d29b4-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d29b4-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d29b4-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d29b4-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="d29b4-120">Объект веб-службы машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="d29b4-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="d29b4-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d29b4-121">-Name</span></span>
<span data-ttu-id="d29b4-122">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d29b4-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d29b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d29b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="d29b4-124">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d29b4-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d29b4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d29b4-125">-Confirm</span></span>
<span data-ttu-id="d29b4-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d29b4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d29b4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d29b4-127">-WhatIf</span></span>
<span data-ttu-id="d29b4-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d29b4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d29b4-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d29b4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d29b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29b4-130">CommonParameters</span></span>
<span data-ttu-id="d29b4-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d29b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29b4-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d29b4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29b4-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d29b4-133">INPUTS</span></span>

### <span data-ttu-id="d29b4-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d29b4-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="d29b4-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d29b4-135">OUTPUTS</span></span>

### <span data-ttu-id="d29b4-136">System. void</span><span class="sxs-lookup"><span data-stu-id="d29b4-136">System.Void</span></span>

## <span data-ttu-id="d29b4-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d29b4-137">NOTES</span></span>
<span data-ttu-id="d29b4-138">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d29b4-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d29b4-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d29b4-139">RELATED LINKS</span></span>
