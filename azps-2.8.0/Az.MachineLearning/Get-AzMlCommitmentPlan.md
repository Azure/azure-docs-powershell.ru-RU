---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: e8c3fbb6f3d5f9ca3592546f4039c484003811f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720459"
---
# <span data-ttu-id="f4ed0-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f4ed0-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="f4ed0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ed0-103">Извлекает сводные данные по одному или нескольким планам обязательств.</span><span class="sxs-lookup"><span data-stu-id="f4ed0-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="f4ed0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4ed0-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4ed0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4ed0-105">DESCRIPTION</span></span>
<span data-ttu-id="f4ed0-106">Получение сведений о плане заобязанностей.</span><span class="sxs-lookup"><span data-stu-id="f4ed0-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="f4ed0-107">В зависимости от переданных параметров командлет возвращает определенный план обязательства, набор планов фиксации для указанной группы ресурсов в текущей подписке или набор планов фиксации в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="f4ed0-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="f4ed0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4ed0-108">EXAMPLES</span></span>

### <span data-ttu-id="f4ed0-109">Пример 1: получение определенного плана обязательства</span><span class="sxs-lookup"><span data-stu-id="f4ed0-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="f4ed0-110">Пример 2: получение всех ресурсов плана обязательств в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="f4ed0-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="f4ed0-111">Пример 3: получение всех планов обязательства в текущей подписке и данной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f4ed0-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="f4ed0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4ed0-112">PARAMETERS</span></span>

### <span data-ttu-id="f4ed0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ed0-113">-DefaultProfile</span></span>
<span data-ttu-id="f4ed0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f4ed0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4ed0-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4ed0-115">-Name</span></span>
<span data-ttu-id="f4ed0-116">Название плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="f4ed0-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="f4ed0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ed0-117">-ResourceGroupName</span></span>
<span data-ttu-id="f4ed0-118">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f4ed0-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f4ed0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ed0-119">CommonParameters</span></span>
<span data-ttu-id="f4ed0-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4ed0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ed0-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ed0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ed0-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4ed0-122">INPUTS</span></span>

### <span data-ttu-id="f4ed0-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="f4ed0-123">None</span></span>

## <span data-ttu-id="f4ed0-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4ed0-124">OUTPUTS</span></span>

### <span data-ttu-id="f4ed0-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f4ed0-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="f4ed0-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4ed0-126">NOTES</span></span>
<span data-ttu-id="f4ed0-127">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f4ed0-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f4ed0-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4ed0-128">RELATED LINKS</span></span>
