---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: b3ea89f2470052a0d5858da199ee5285b3d5ea18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965827"
---
# <span data-ttu-id="f694b-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f694b-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="f694b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f694b-102">SYNOPSIS</span></span>
<span data-ttu-id="f694b-103">Извлекает сводную информацию для одного или более планов обязательств.</span><span class="sxs-lookup"><span data-stu-id="f694b-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="f694b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f694b-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f694b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f694b-105">DESCRIPTION</span></span>
<span data-ttu-id="f694b-106">Извлекает сведения о плане обязательств.</span><span class="sxs-lookup"><span data-stu-id="f694b-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="f694b-107">В зависимости от переданных параметров он возвращает определенный план обязательств, набор планов обязательств для указанной группы ресурсов в текущей подписке или набор планов обязательств в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="f694b-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="f694b-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f694b-108">EXAMPLES</span></span>

### <span data-ttu-id="f694b-109">Пример 1. Получите определенный план обязательств</span><span class="sxs-lookup"><span data-stu-id="f694b-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="f694b-110">Пример 2. Получить все ресурсы по плану обязательств в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="f694b-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="f694b-111">Пример 3. Получите все планы обязательств в текущей подписке и предоставленную группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="f694b-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="f694b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f694b-112">PARAMETERS</span></span>

### <span data-ttu-id="f694b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f694b-113">-DefaultProfile</span></span>
<span data-ttu-id="f694b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f694b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f694b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f694b-115">-Name</span></span>
<span data-ttu-id="f694b-116">Название плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="f694b-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="f694b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f694b-117">-ResourceGroupName</span></span>
<span data-ttu-id="f694b-118">Имя группы ресурсов для плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f694b-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f694b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f694b-119">CommonParameters</span></span>
<span data-ttu-id="f694b-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f694b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f694b-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f694b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f694b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f694b-122">INPUTS</span></span>

### <span data-ttu-id="f694b-123">Нет</span><span class="sxs-lookup"><span data-stu-id="f694b-123">None</span></span>

## <span data-ttu-id="f694b-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f694b-124">OUTPUTS</span></span>

### <span data-ttu-id="f694b-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f694b-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="f694b-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f694b-126">NOTES</span></span>
<span data-ttu-id="f694b-127">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f694b-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f694b-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f694b-128">RELATED LINKS</span></span>
