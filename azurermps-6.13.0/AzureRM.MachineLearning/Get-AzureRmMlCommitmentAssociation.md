---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 5535ccb243b6c49d95f06c8cd13cf95bab52abe7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565393"
---
# <span data-ttu-id="76c99-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="76c99-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="76c99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76c99-102">SYNOPSIS</span></span>
<span data-ttu-id="76c99-103">Извлекает сводные данные по одной или нескольким ассоциациям обязательства.</span><span class="sxs-lookup"><span data-stu-id="76c99-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76c99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76c99-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c99-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76c99-105">DESCRIPTION</span></span>
<span data-ttu-id="76c99-106">Получение сведений о сопоставлении обязательства.</span><span class="sxs-lookup"><span data-stu-id="76c99-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="76c99-107">В зависимости от переданных параметров, командлет возвращает определенную связь обязательства или коллекцию сопоставлений обязательства для указанного плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="76c99-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="76c99-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76c99-108">EXAMPLES</span></span>

### <span data-ttu-id="76c99-109">Пример 1: получение конкретной связи обязательства</span><span class="sxs-lookup"><span data-stu-id="76c99-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="76c99-110">Пример 2: получение всех связей обязательства для указанного плана обязательства</span><span class="sxs-lookup"><span data-stu-id="76c99-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="76c99-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76c99-111">PARAMETERS</span></span>

### <span data-ttu-id="76c99-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="76c99-112">-CommitmentPlanName</span></span>
<span data-ttu-id="76c99-113">Имя плана фиксации Azure ML с одной или несколькими связями о обязательствах.</span><span class="sxs-lookup"><span data-stu-id="76c99-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="76c99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c99-114">-DefaultProfile</span></span>
<span data-ttu-id="76c99-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="76c99-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76c99-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76c99-116">-Name</span></span>
<span data-ttu-id="76c99-117">Имя сопоставления фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="76c99-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="76c99-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c99-118">-ResourceGroupName</span></span>
<span data-ttu-id="76c99-119">Имя группы ресурсов для ассоциации обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="76c99-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="76c99-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c99-120">CommonParameters</span></span>
<span data-ttu-id="76c99-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76c99-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c99-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c99-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c99-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76c99-123">INPUTS</span></span>

### <span data-ttu-id="76c99-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="76c99-124">None</span></span>

## <span data-ttu-id="76c99-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76c99-125">OUTPUTS</span></span>

### <span data-ttu-id="76c99-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="76c99-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="76c99-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="76c99-127">NOTES</span></span>
<span data-ttu-id="76c99-128">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="76c99-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="76c99-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76c99-129">RELATED LINKS</span></span>
