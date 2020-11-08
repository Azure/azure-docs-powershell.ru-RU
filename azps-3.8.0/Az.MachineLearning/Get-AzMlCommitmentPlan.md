---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074246"
---
# <span data-ttu-id="5e8b7-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="5e8b7-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="5e8b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8b7-103">Извлекает сводные данные по одному или нескольким планам обязательств.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="5e8b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e8b7-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e8b7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e8b7-105">DESCRIPTION</span></span>
<span data-ttu-id="5e8b7-106">Получение сведений о плане заобязанностей.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="5e8b7-107">В зависимости от переданных параметров командлет возвращает определенный план обязательства, набор планов фиксации для указанной группы ресурсов в текущей подписке или набор планов фиксации в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="5e8b7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e8b7-108">EXAMPLES</span></span>

### <span data-ttu-id="5e8b7-109">Пример 1: получение определенного плана обязательства</span><span class="sxs-lookup"><span data-stu-id="5e8b7-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="5e8b7-110">Пример 2: получение всех ресурсов плана обязательств в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="5e8b7-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="5e8b7-111">Пример 3: получение всех планов обязательства в текущей подписке и данной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5e8b7-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="5e8b7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e8b7-112">PARAMETERS</span></span>

### <span data-ttu-id="5e8b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8b7-113">-DefaultProfile</span></span>
<span data-ttu-id="5e8b7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5e8b7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e8b7-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e8b7-115">-Name</span></span>
<span data-ttu-id="5e8b7-116">Название плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="5e8b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e8b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e8b7-118">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="5e8b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8b7-119">CommonParameters</span></span>
<span data-ttu-id="5e8b7-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8b7-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e8b7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8b7-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e8b7-122">INPUTS</span></span>

### <span data-ttu-id="5e8b7-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="5e8b7-123">None</span></span>

## <span data-ttu-id="5e8b7-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e8b7-124">OUTPUTS</span></span>

### <span data-ttu-id="5e8b7-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="5e8b7-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="5e8b7-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e8b7-126">NOTES</span></span>
<span data-ttu-id="5e8b7-127">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5e8b7-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5e8b7-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e8b7-128">RELATED LINKS</span></span>
