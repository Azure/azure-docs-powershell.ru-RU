---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 3be16cd371543848d650711241dbcb8828a5ba32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568573"
---
# <span data-ttu-id="55f3a-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="55f3a-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="55f3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="55f3a-103">Извлекает сводные данные по одной или нескольким ассоциациям обязательства.</span><span class="sxs-lookup"><span data-stu-id="55f3a-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55f3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55f3a-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55f3a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="55f3a-106">Получение сведений о сопоставлении обязательства.</span><span class="sxs-lookup"><span data-stu-id="55f3a-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="55f3a-107">В зависимости от переданных параметров, командлет возвращает определенную связь обязательства или коллекцию сопоставлений обязательства для указанного плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="55f3a-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="55f3a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55f3a-108">EXAMPLES</span></span>

### <span data-ttu-id="55f3a-109">--------------------------Пример 1: получение соответствия определенным обязательствам--------------------------</span><span class="sxs-lookup"><span data-stu-id="55f3a-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="55f3a-110">--------------------------Пример 2: получение всех сопоставлений по обязательствам для указанного плана обязательства--------------------------</span><span class="sxs-lookup"><span data-stu-id="55f3a-110">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="55f3a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55f3a-111">PARAMETERS</span></span>

### <span data-ttu-id="55f3a-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="55f3a-112">-CommitmentPlanName</span></span>
<span data-ttu-id="55f3a-113">Имя плана фиксации Azure ML с одной или несколькими связями о обязательствах.</span><span class="sxs-lookup"><span data-stu-id="55f3a-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="55f3a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f3a-114">-DefaultProfile</span></span>
<span data-ttu-id="55f3a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="55f3a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55f3a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55f3a-116">-Name</span></span>
<span data-ttu-id="55f3a-117">Имя сопоставления фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="55f3a-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f3a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f3a-118">-ResourceGroupName</span></span>
<span data-ttu-id="55f3a-119">Имя группы ресурсов для ассоциации обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="55f3a-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="55f3a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f3a-120">CommonParameters</span></span>
<span data-ttu-id="55f3a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55f3a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f3a-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55f3a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f3a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55f3a-123">INPUTS</span></span>

### <span data-ttu-id="55f3a-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="55f3a-124">None</span></span>
<span data-ttu-id="55f3a-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="55f3a-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55f3a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55f3a-126">OUTPUTS</span></span>

### <span data-ttu-id="55f3a-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="55f3a-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="55f3a-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="55f3a-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="55f3a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="55f3a-129">NOTES</span></span>
<span data-ttu-id="55f3a-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="55f3a-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="55f3a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55f3a-131">RELATED LINKS</span></span>

