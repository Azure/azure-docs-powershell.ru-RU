---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 31678552a43951406d18c49ee80ffaa7897fd1d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735159"
---
# <span data-ttu-id="12e76-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="12e76-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="12e76-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12e76-102">SYNOPSIS</span></span>
<span data-ttu-id="12e76-103">Удаление плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="12e76-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12e76-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12e76-104">SYNTAX</span></span>

### <span data-ttu-id="12e76-105">Удаление плана фиксации Azure ML, указанного по имени и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12e76-105">Remove an Azure ML commitment plan specified by name and resource group.</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e76-106">Удаление плана фиксации Azure ML, указанного в качестве объекта.</span><span class="sxs-lookup"><span data-stu-id="12e76-106">Remove an Azure ML commitment plan specified as an object.</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12e76-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12e76-107">DESCRIPTION</span></span>
<span data-ttu-id="12e76-108">Удаление плана фиксации машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="12e76-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="12e76-109">Обратите внимание, что планы обязательства, в которых есть связи обязательства, нельзя удалить.</span><span class="sxs-lookup"><span data-stu-id="12e76-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="12e76-110">Ассоциации обязательства можно удалить только по целевому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="12e76-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="12e76-111">Например, если вы удалите веб-службу машинного обучения Azure, она также будет удалена, так как связь по обязательствам, связывающая веб-службу с планом фиксации.</span><span class="sxs-lookup"><span data-stu-id="12e76-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="12e76-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12e76-112">EXAMPLES</span></span>

### <span data-ttu-id="12e76-113">--------------------------Пример 1: Удаление плана обязательства--------------------------</span><span class="sxs-lookup"><span data-stu-id="12e76-113">--------------------------  Example 1: Delete a commitment plan  --------------------------</span></span>
<span data-ttu-id="12e76-114">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="12e76-114">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="12e76-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12e76-115">PARAMETERS</span></span>

### <span data-ttu-id="12e76-116">-Force</span><span class="sxs-lookup"><span data-stu-id="12e76-116">-Force</span></span>
<span data-ttu-id="12e76-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="12e76-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="12e76-118">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="12e76-118">-MlCommitmentPlan</span></span>
<span data-ttu-id="12e76-119">Объект веб-службы машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="12e76-119">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: Remove an Azure ML commitment plan specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12e76-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12e76-120">-Name</span></span>
<span data-ttu-id="12e76-121">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="12e76-121">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e76-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e76-122">-ResourceGroupName</span></span>
<span data-ttu-id="12e76-123">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="12e76-123">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e76-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12e76-124">-Confirm</span></span>
<span data-ttu-id="12e76-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="12e76-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e76-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e76-126">-WhatIf</span></span>
<span data-ttu-id="12e76-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="12e76-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12e76-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12e76-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e76-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e76-129">-DefaultProfile</span></span>
<span data-ttu-id="12e76-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12e76-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12e76-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e76-131">CommonParameters</span></span>
<span data-ttu-id="12e76-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12e76-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e76-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e76-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e76-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12e76-134">INPUTS</span></span>

### <span data-ttu-id="12e76-135">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="12e76-135">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="12e76-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12e76-136">OUTPUTS</span></span>

### <span data-ttu-id="12e76-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="12e76-137">None</span></span>

## <span data-ttu-id="12e76-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="12e76-138">NOTES</span></span>
<span data-ttu-id="12e76-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="12e76-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="12e76-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12e76-140">RELATED LINKS</span></span>

