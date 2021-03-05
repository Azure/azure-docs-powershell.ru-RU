---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 287db082c5cbe842b0a92b124870effb77068912
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960552"
---
# <span data-ttu-id="b564e-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b564e-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="b564e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b564e-102">SYNOPSIS</span></span>
<span data-ttu-id="b564e-103">Удаляет план обязательств.</span><span class="sxs-lookup"><span data-stu-id="b564e-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="b564e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b564e-104">SYNTAX</span></span>

### <span data-ttu-id="b564e-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b564e-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b564e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="b564e-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b564e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b564e-107">DESCRIPTION</span></span>
<span data-ttu-id="b564e-108">Удаляет план обязательств по машинным обучению Azure.</span><span class="sxs-lookup"><span data-stu-id="b564e-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="b564e-109">Обратите внимание на то, что планы обязательств, которые имеют связи обязательств, невозможно удалить.</span><span class="sxs-lookup"><span data-stu-id="b564e-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="b564e-110">Связи обязательств можно удалить только для целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="b564e-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="b564e-111">Например, при удалении веб-службы машинного обучения Azure связь обязательств, которая связывает веб-службу с планом обязательств, также будет удалена.</span><span class="sxs-lookup"><span data-stu-id="b564e-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="b564e-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b564e-112">EXAMPLES</span></span>

### <span data-ttu-id="b564e-113">Пример 1. Удаление плана обязательств</span><span class="sxs-lookup"><span data-stu-id="b564e-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="b564e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b564e-114">PARAMETERS</span></span>

### <span data-ttu-id="b564e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b564e-115">-DefaultProfile</span></span>
<span data-ttu-id="b564e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b564e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b564e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b564e-117">-Force</span></span>
<span data-ttu-id="b564e-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b564e-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b564e-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b564e-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="b564e-120">Объект веб-службы машинного обучения.</span><span class="sxs-lookup"><span data-stu-id="b564e-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="b564e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b564e-121">-Name</span></span>
<span data-ttu-id="b564e-122">Имя плана обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b564e-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b564e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b564e-123">-ResourceGroupName</span></span>
<span data-ttu-id="b564e-124">Имя группы ресурсов для плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="b564e-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b564e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b564e-125">-Confirm</span></span>
<span data-ttu-id="b564e-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b564e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b564e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b564e-127">-WhatIf</span></span>
<span data-ttu-id="b564e-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b564e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b564e-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b564e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b564e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b564e-130">CommonParameters</span></span>
<span data-ttu-id="b564e-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b564e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b564e-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b564e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b564e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b564e-133">INPUTS</span></span>

### <span data-ttu-id="b564e-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="b564e-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="b564e-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b564e-135">OUTPUTS</span></span>

### <span data-ttu-id="b564e-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="b564e-136">System.Void</span></span>

## <span data-ttu-id="b564e-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b564e-137">NOTES</span></span>
<span data-ttu-id="b564e-138">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b564e-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b564e-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b564e-139">RELATED LINKS</span></span>
