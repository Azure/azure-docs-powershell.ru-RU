---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: f0b081911d1bcd2a2b195d3185eb3b36505060c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732716"
---
# <span data-ttu-id="ac704-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ac704-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="ac704-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac704-102">SYNOPSIS</span></span>
<span data-ttu-id="ac704-103">Извлекает сводные данные по одному или нескольким планам обязательств.</span><span class="sxs-lookup"><span data-stu-id="ac704-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac704-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac704-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac704-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac704-105">DESCRIPTION</span></span>
<span data-ttu-id="ac704-106">Получение сведений о плане заобязанностей.</span><span class="sxs-lookup"><span data-stu-id="ac704-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="ac704-107">В зависимости от переданных параметров, командлет возвращает определенный план фиксации, набор планов фиксации для указанной группы ресурсов в текущей подписке или набор планов обязательства в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="ac704-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="ac704-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac704-108">EXAMPLES</span></span>

### <span data-ttu-id="ac704-109">Пример 1: получение определенного плана обязательства</span><span class="sxs-lookup"><span data-stu-id="ac704-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="ac704-110">Пример 2: получение всех ресурсов плана обязательств в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="ac704-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="ac704-111">Пример 3: получение всех планов обязательства в текущей подписке и данной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="ac704-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="ac704-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac704-112">PARAMETERS</span></span>

### <span data-ttu-id="ac704-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac704-113">-DefaultProfile</span></span>
<span data-ttu-id="ac704-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ac704-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac704-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac704-115">-Name</span></span>
<span data-ttu-id="ac704-116">Название плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="ac704-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="ac704-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac704-117">-ResourceGroupName</span></span>
<span data-ttu-id="ac704-118">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ac704-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ac704-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac704-119">CommonParameters</span></span>
<span data-ttu-id="ac704-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac704-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac704-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac704-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac704-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac704-122">INPUTS</span></span>

### <span data-ttu-id="ac704-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="ac704-123">None</span></span>

## <span data-ttu-id="ac704-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac704-124">OUTPUTS</span></span>

### <span data-ttu-id="ac704-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ac704-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="ac704-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac704-126">NOTES</span></span>
<span data-ttu-id="ac704-127">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ac704-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ac704-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac704-128">RELATED LINKS</span></span>
