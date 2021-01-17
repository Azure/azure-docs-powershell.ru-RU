---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405911"
---
# <span data-ttu-id="e5d21-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="e5d21-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="e5d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5d21-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d21-103">Перемещает связь обязательств из одного плана обязательств в другой.</span><span class="sxs-lookup"><span data-stu-id="e5d21-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="e5d21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5d21-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5d21-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5d21-105">DESCRIPTION</span></span>
<span data-ttu-id="e5d21-106">Перемещает ресурс связи обязательств из своего родительского плана в другой план обязательств.</span><span class="sxs-lookup"><span data-stu-id="e5d21-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="e5d21-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5d21-107">EXAMPLES</span></span>

### <span data-ttu-id="e5d21-108">Пример 1. Перемещение связи обязательства</span><span class="sxs-lookup"><span data-stu-id="e5d21-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="e5d21-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5d21-109">PARAMETERS</span></span>

### <span data-ttu-id="e5d21-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="e5d21-110">-CommitmentPlanName</span></span>
<span data-ttu-id="e5d21-111">Имя плана обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e5d21-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e5d21-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d21-112">-DefaultProfile</span></span>
<span data-ttu-id="e5d21-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e5d21-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5d21-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="e5d21-114">-DestinationPlanId</span></span>
<span data-ttu-id="e5d21-115">ИД ресурсов Azure конечного плана обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e5d21-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e5d21-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e5d21-116">-Name</span></span>
<span data-ttu-id="e5d21-117">Имя связи обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e5d21-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e5d21-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5d21-118">-ResourceGroupName</span></span>
<span data-ttu-id="e5d21-119">Имя группы ресурсов для связи обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="e5d21-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e5d21-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5d21-120">-Confirm</span></span>
<span data-ttu-id="e5d21-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e5d21-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5d21-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5d21-122">-WhatIf</span></span>
<span data-ttu-id="e5d21-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5d21-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5d21-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e5d21-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5d21-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d21-125">CommonParameters</span></span>
<span data-ttu-id="e5d21-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d21-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d21-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5d21-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d21-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5d21-128">INPUTS</span></span>

### <span data-ttu-id="e5d21-129">Нет</span><span class="sxs-lookup"><span data-stu-id="e5d21-129">None</span></span>

## <span data-ttu-id="e5d21-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5d21-130">OUTPUTS</span></span>

### <span data-ttu-id="e5d21-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="e5d21-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="e5d21-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5d21-132">NOTES</span></span>
<span data-ttu-id="e5d21-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e5d21-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e5d21-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5d21-134">RELATED LINKS</span></span>
