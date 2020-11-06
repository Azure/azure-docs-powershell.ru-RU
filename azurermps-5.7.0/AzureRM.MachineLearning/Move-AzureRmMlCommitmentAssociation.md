---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 2bd650e86a1a4b59694dc88dc915da0fd7713e5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569960"
---
# <span data-ttu-id="78da5-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="78da5-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="78da5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78da5-102">SYNOPSIS</span></span>
<span data-ttu-id="78da5-103">Перемещает сопоставление обязательства из одного плана обязательства в другой.</span><span class="sxs-lookup"><span data-stu-id="78da5-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78da5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78da5-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78da5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78da5-105">DESCRIPTION</span></span>
<span data-ttu-id="78da5-106">Перемещает ресурс связи обязательства из плана родительского обязательства в другой план обязательств.</span><span class="sxs-lookup"><span data-stu-id="78da5-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="78da5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78da5-107">EXAMPLES</span></span>

### <span data-ttu-id="78da5-108">--------------------------Примере 1: Перенесите соответствие обязательствам--------------------------</span><span class="sxs-lookup"><span data-stu-id="78da5-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="78da5-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78da5-109">PARAMETERS</span></span>

### <span data-ttu-id="78da5-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="78da5-110">-CommitmentPlanName</span></span>
<span data-ttu-id="78da5-111">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="78da5-111">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78da5-112">-DefaultProfile</span></span>
<span data-ttu-id="78da5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="78da5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da5-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="78da5-114">-DestinationPlanId</span></span>
<span data-ttu-id="78da5-115">Идентификатор ресурса Azure целевого плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="78da5-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da5-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78da5-116">-Name</span></span>
<span data-ttu-id="78da5-117">Имя сопоставления фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="78da5-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78da5-118">-ResourceGroupName</span></span>
<span data-ttu-id="78da5-119">Имя группы ресурсов для ассоциации обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="78da5-119">The name of the resource group for the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da5-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78da5-120">-Confirm</span></span>
<span data-ttu-id="78da5-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78da5-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78da5-122">-WhatIf</span></span>
<span data-ttu-id="78da5-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78da5-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78da5-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78da5-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78da5-125">CommonParameters</span></span>
<span data-ttu-id="78da5-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78da5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78da5-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78da5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78da5-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78da5-128">INPUTS</span></span>

### <span data-ttu-id="78da5-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="78da5-129">None</span></span>
<span data-ttu-id="78da5-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="78da5-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78da5-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78da5-131">OUTPUTS</span></span>

### <span data-ttu-id="78da5-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="78da5-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="78da5-133">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="78da5-133">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="78da5-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="78da5-134">NOTES</span></span>
<span data-ttu-id="78da5-135">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="78da5-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="78da5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78da5-136">RELATED LINKS</span></span>

