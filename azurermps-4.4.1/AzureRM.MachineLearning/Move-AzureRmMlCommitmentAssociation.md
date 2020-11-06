---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 84c1560cf4d97f7a40735d767c2c4d82fcd7d65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569356"
---
# <span data-ttu-id="6ad74-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="6ad74-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="6ad74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ad74-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad74-103">Перемещает сопоставление обязательства из одного плана обязательства в другой.</span><span class="sxs-lookup"><span data-stu-id="6ad74-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ad74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ad74-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ad74-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ad74-105">DESCRIPTION</span></span>
<span data-ttu-id="6ad74-106">Перемещает ресурс связи обязательства из плана родительского обязательства в другой план обязательств.</span><span class="sxs-lookup"><span data-stu-id="6ad74-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="6ad74-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ad74-107">EXAMPLES</span></span>

### <span data-ttu-id="6ad74-108">--------------------------Примере 1: Перенесите соответствие обязательствам--------------------------</span><span class="sxs-lookup"><span data-stu-id="6ad74-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
<span data-ttu-id="6ad74-109">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="6ad74-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="6ad74-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ad74-110">PARAMETERS</span></span>

### <span data-ttu-id="6ad74-111">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="6ad74-111">-CommitmentPlanName</span></span>
<span data-ttu-id="6ad74-112">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6ad74-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6ad74-113">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="6ad74-113">-DestinationPlanId</span></span>
<span data-ttu-id="6ad74-114">Идентификатор ресурса Azure целевого плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6ad74-114">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6ad74-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6ad74-115">-Name</span></span>
<span data-ttu-id="6ad74-116">Имя сопоставления фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6ad74-116">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="6ad74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad74-117">-ResourceGroupName</span></span>
<span data-ttu-id="6ad74-118">Имя группы ресурсов для ассоциации обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="6ad74-118">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="6ad74-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ad74-119">-Confirm</span></span>
<span data-ttu-id="6ad74-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6ad74-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad74-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad74-121">-WhatIf</span></span>
<span data-ttu-id="6ad74-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6ad74-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ad74-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ad74-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad74-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad74-124">-DefaultProfile</span></span>
<span data-ttu-id="6ad74-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ad74-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ad74-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad74-126">CommonParameters</span></span>
<span data-ttu-id="6ad74-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ad74-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad74-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad74-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad74-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ad74-129">INPUTS</span></span>

## <span data-ttu-id="6ad74-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ad74-130">OUTPUTS</span></span>

### <span data-ttu-id="6ad74-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6ad74-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="6ad74-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="6ad74-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="6ad74-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ad74-133">NOTES</span></span>
<span data-ttu-id="6ad74-134">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="6ad74-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6ad74-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ad74-135">RELATED LINKS</span></span>

