---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226345"
---
# <span data-ttu-id="e0dac-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="e0dac-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="e0dac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0dac-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dac-103">Перемещает связь обязательств из одного плана обязательств в другой.</span><span class="sxs-lookup"><span data-stu-id="e0dac-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="e0dac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0dac-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0dac-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0dac-105">DESCRIPTION</span></span>
<span data-ttu-id="e0dac-106">Перемещает ресурс связи обязательств из своего родительского плана в другой план обязательств.</span><span class="sxs-lookup"><span data-stu-id="e0dac-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="e0dac-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0dac-107">EXAMPLES</span></span>

### <span data-ttu-id="e0dac-108">Пример 1. Перемещение связи обязательства</span><span class="sxs-lookup"><span data-stu-id="e0dac-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="e0dac-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0dac-109">PARAMETERS</span></span>

### <span data-ttu-id="e0dac-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="e0dac-110">-CommitmentPlanName</span></span>
<span data-ttu-id="e0dac-111">Имя плана обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e0dac-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e0dac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dac-112">-DefaultProfile</span></span>
<span data-ttu-id="e0dac-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e0dac-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0dac-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="e0dac-114">-DestinationPlanId</span></span>
<span data-ttu-id="e0dac-115">ИД ресурсов Azure конечного плана обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e0dac-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e0dac-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e0dac-116">-Name</span></span>
<span data-ttu-id="e0dac-117">Имя связи обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e0dac-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e0dac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0dac-118">-ResourceGroupName</span></span>
<span data-ttu-id="e0dac-119">Имя группы ресурсов для связи обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e0dac-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e0dac-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0dac-120">-Confirm</span></span>
<span data-ttu-id="e0dac-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0dac-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0dac-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0dac-122">-WhatIf</span></span>
<span data-ttu-id="e0dac-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0dac-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0dac-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e0dac-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0dac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dac-125">CommonParameters</span></span>
<span data-ttu-id="e0dac-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0dac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dac-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0dac-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dac-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0dac-128">INPUTS</span></span>

### <span data-ttu-id="e0dac-129">Нет</span><span class="sxs-lookup"><span data-stu-id="e0dac-129">None</span></span>

## <span data-ttu-id="e0dac-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0dac-130">OUTPUTS</span></span>

### <span data-ttu-id="e0dac-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="e0dac-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="e0dac-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0dac-132">NOTES</span></span>
<span data-ttu-id="e0dac-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e0dac-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e0dac-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0dac-134">RELATED LINKS</span></span>
