---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 5404cf82308c63a5ba6fe07ef4ac01101f44c48c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734444"
---
# <span data-ttu-id="d9d6c-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d9d6c-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="d9d6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d6c-103">Извлекает сводные данные по одному или нескольким планам обязательств.</span><span class="sxs-lookup"><span data-stu-id="d9d6c-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9d6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9d6c-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9d6c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="d9d6c-106">Получение сведений о плане заобязанностей.</span><span class="sxs-lookup"><span data-stu-id="d9d6c-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="d9d6c-107">В зависимости от переданных параметров, командлет возвращает определенный план фиксации, набор планов фиксации для указанной группы ресурсов в текущей подписке или набор планов обязательства в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="d9d6c-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="d9d6c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9d6c-108">EXAMPLES</span></span>

### <span data-ttu-id="d9d6c-109">--------------------------Пример 1: получение плана для определенного обязательства--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9d6c-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="d9d6c-110">--------------------------Пример 2: получение всех ресурсов плана обязательств в текущей подписке--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9d6c-110">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="d9d6c-111">--------------------------Пример 3: получение всех планов обязательства в текущей подписке и данной группе ресурсов--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9d6c-111">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="d9d6c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9d6c-112">PARAMETERS</span></span>

### <span data-ttu-id="d9d6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d6c-113">-DefaultProfile</span></span>
<span data-ttu-id="d9d6c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d9d6c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9d6c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9d6c-115">-Name</span></span>
<span data-ttu-id="d9d6c-116">Название плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="d9d6c-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="d9d6c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d6c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9d6c-118">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d9d6c-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="d9d6c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d6c-119">CommonParameters</span></span>
<span data-ttu-id="d9d6c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9d6c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d6c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d6c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d6c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9d6c-122">INPUTS</span></span>

### <span data-ttu-id="d9d6c-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="d9d6c-123">None</span></span>
<span data-ttu-id="d9d6c-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d9d6c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9d6c-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9d6c-125">OUTPUTS</span></span>

### <span data-ttu-id="d9d6c-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d9d6c-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="d9d6c-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="d9d6c-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="d9d6c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9d6c-128">NOTES</span></span>
<span data-ttu-id="d9d6c-129">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d9d6c-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d9d6c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9d6c-130">RELATED LINKS</span></span>

