---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: d22632f830c40cd992f874d4f09c05b8a3fd9a5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899797"
---
# <span data-ttu-id="bef7a-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="bef7a-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="bef7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bef7a-102">SYNOPSIS</span></span>
<span data-ttu-id="bef7a-103">Извлекает сводные данные по одной или нескольким ассоциациям обязательства.</span><span class="sxs-lookup"><span data-stu-id="bef7a-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="bef7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bef7a-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bef7a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bef7a-105">DESCRIPTION</span></span>
<span data-ttu-id="bef7a-106">Получение сведений о сопоставлении обязательства.</span><span class="sxs-lookup"><span data-stu-id="bef7a-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="bef7a-107">В зависимости от переданных параметров, командлет возвращает определенную связь обязательства или коллекцию сопоставлений обязательства для указанного плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="bef7a-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="bef7a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bef7a-108">EXAMPLES</span></span>

### <span data-ttu-id="bef7a-109">Пример 1: получение конкретной связи обязательства</span><span class="sxs-lookup"><span data-stu-id="bef7a-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="bef7a-110">Пример 2: получение всех связей обязательства для указанного плана обязательства</span><span class="sxs-lookup"><span data-stu-id="bef7a-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="bef7a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bef7a-111">PARAMETERS</span></span>

### <span data-ttu-id="bef7a-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="bef7a-112">-CommitmentPlanName</span></span>
<span data-ttu-id="bef7a-113">Имя плана фиксации Azure ML с одной или несколькими связями о обязательствах.</span><span class="sxs-lookup"><span data-stu-id="bef7a-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="bef7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef7a-114">-DefaultProfile</span></span>
<span data-ttu-id="bef7a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bef7a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bef7a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bef7a-116">-Name</span></span>
<span data-ttu-id="bef7a-117">Имя сопоставления фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="bef7a-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef7a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bef7a-118">-ResourceGroupName</span></span>
<span data-ttu-id="bef7a-119">Имя группы ресурсов для ассоциации обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="bef7a-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="bef7a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef7a-120">CommonParameters</span></span>
<span data-ttu-id="bef7a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bef7a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef7a-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef7a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef7a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bef7a-123">INPUTS</span></span>

### <span data-ttu-id="bef7a-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="bef7a-124">None</span></span>

## <span data-ttu-id="bef7a-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bef7a-125">OUTPUTS</span></span>

### <span data-ttu-id="bef7a-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="bef7a-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="bef7a-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="bef7a-127">NOTES</span></span>
<span data-ttu-id="bef7a-128">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="bef7a-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="bef7a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bef7a-129">RELATED LINKS</span></span>
