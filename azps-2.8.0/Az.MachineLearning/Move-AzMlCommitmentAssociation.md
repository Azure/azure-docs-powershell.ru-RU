---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: 96f686fe395ce20d4eabe32f8df2b5821384ab0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720441"
---
# <span data-ttu-id="dae41-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="dae41-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="dae41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dae41-102">SYNOPSIS</span></span>
<span data-ttu-id="dae41-103">Перемещает сопоставление обязательства из одного плана обязательства в другой.</span><span class="sxs-lookup"><span data-stu-id="dae41-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="dae41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dae41-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dae41-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dae41-105">DESCRIPTION</span></span>
<span data-ttu-id="dae41-106">Перемещает ресурс связи обязательства из плана родительского обязательства в другой план обязательств.</span><span class="sxs-lookup"><span data-stu-id="dae41-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="dae41-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dae41-107">EXAMPLES</span></span>

### <span data-ttu-id="dae41-108">Пример 1: перемещение связи обязательства</span><span class="sxs-lookup"><span data-stu-id="dae41-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="dae41-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dae41-109">PARAMETERS</span></span>

### <span data-ttu-id="dae41-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="dae41-110">-CommitmentPlanName</span></span>
<span data-ttu-id="dae41-111">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dae41-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dae41-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae41-112">-DefaultProfile</span></span>
<span data-ttu-id="dae41-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dae41-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dae41-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="dae41-114">-DestinationPlanId</span></span>
<span data-ttu-id="dae41-115">Идентификатор ресурса Azure целевого плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dae41-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dae41-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dae41-116">-Name</span></span>
<span data-ttu-id="dae41-117">Имя сопоставления фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dae41-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="dae41-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae41-118">-ResourceGroupName</span></span>
<span data-ttu-id="dae41-119">Имя группы ресурсов для ассоциации обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="dae41-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="dae41-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dae41-120">-Confirm</span></span>
<span data-ttu-id="dae41-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dae41-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dae41-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae41-122">-WhatIf</span></span>
<span data-ttu-id="dae41-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dae41-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dae41-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dae41-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dae41-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae41-125">CommonParameters</span></span>
<span data-ttu-id="dae41-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dae41-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae41-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dae41-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae41-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dae41-128">INPUTS</span></span>

### <span data-ttu-id="dae41-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="dae41-129">None</span></span>

## <span data-ttu-id="dae41-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dae41-130">OUTPUTS</span></span>

### <span data-ttu-id="dae41-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dae41-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="dae41-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="dae41-132">NOTES</span></span>
<span data-ttu-id="dae41-133">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="dae41-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dae41-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dae41-134">RELATED LINKS</span></span>
