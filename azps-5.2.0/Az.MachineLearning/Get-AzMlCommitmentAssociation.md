---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400180"
---
# <span data-ttu-id="48770-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="48770-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="48770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48770-102">SYNOPSIS</span></span>
<span data-ttu-id="48770-103">Извлекает сводную информацию по одному или несколько связи обязательств.</span><span class="sxs-lookup"><span data-stu-id="48770-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="48770-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="48770-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48770-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48770-105">DESCRIPTION</span></span>
<span data-ttu-id="48770-106">Извлекает сведения об связи обязательств.</span><span class="sxs-lookup"><span data-stu-id="48770-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="48770-107">В зависимости от переданных параметров он возвращает связь определенного обязательства или набор связи обязательств для указанного плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="48770-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="48770-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="48770-108">EXAMPLES</span></span>

### <span data-ttu-id="48770-109">Пример 1. Связь с определенными обязательствами</span><span class="sxs-lookup"><span data-stu-id="48770-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="48770-110">Пример 2. Получить связи всех обязательств для указанного плана обязательств</span><span class="sxs-lookup"><span data-stu-id="48770-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="48770-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48770-111">PARAMETERS</span></span>

### <span data-ttu-id="48770-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="48770-112">-CommitmentPlanName</span></span>
<span data-ttu-id="48770-113">Название плана обязательства Azure ML, который имеет одну или несколько связи обязательств.</span><span class="sxs-lookup"><span data-stu-id="48770-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="48770-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48770-114">-DefaultProfile</span></span>
<span data-ttu-id="48770-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="48770-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48770-116">-Name</span><span class="sxs-lookup"><span data-stu-id="48770-116">-Name</span></span>
<span data-ttu-id="48770-117">Имя связи обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="48770-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="48770-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48770-118">-ResourceGroupName</span></span>
<span data-ttu-id="48770-119">Имя группы ресурсов для связи обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="48770-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="48770-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48770-120">CommonParameters</span></span>
<span data-ttu-id="48770-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48770-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48770-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48770-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48770-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48770-123">INPUTS</span></span>

### <span data-ttu-id="48770-124">Нет</span><span class="sxs-lookup"><span data-stu-id="48770-124">None</span></span>

## <span data-ttu-id="48770-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="48770-125">OUTPUTS</span></span>

### <span data-ttu-id="48770-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="48770-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="48770-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="48770-127">NOTES</span></span>
<span data-ttu-id="48770-128">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="48770-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="48770-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48770-129">RELATED LINKS</span></span>
