---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221609"
---
# <span data-ttu-id="f3132-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="f3132-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="f3132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3132-102">SYNOPSIS</span></span>
<span data-ttu-id="f3132-103">Извлекает сведения из истории использования для указанного плана обязательств.</span><span class="sxs-lookup"><span data-stu-id="f3132-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="f3132-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3132-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3132-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3132-105">DESCRIPTION</span></span>
<span data-ttu-id="f3132-106">Извлекает сведения из истории использования для указанного плана обязательств, в том числе используемые ресурсы и оставшиеся в нем ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f3132-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="f3132-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3132-107">EXAMPLES</span></span>

### <span data-ttu-id="f3132-108">Пример 1. Получить историю использования для определенного плана обязательств</span><span class="sxs-lookup"><span data-stu-id="f3132-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="f3132-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3132-109">PARAMETERS</span></span>

### <span data-ttu-id="f3132-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3132-110">-DefaultProfile</span></span>
<span data-ttu-id="f3132-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f3132-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3132-112">-Name</span><span class="sxs-lookup"><span data-stu-id="f3132-112">-Name</span></span>
<span data-ttu-id="f3132-113">Имя плана обязательства Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f3132-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f3132-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3132-114">-ResourceGroupName</span></span>
<span data-ttu-id="f3132-115">Имя группы ресурсов для плана обязательств Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f3132-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="f3132-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3132-116">CommonParameters</span></span>
<span data-ttu-id="f3132-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3132-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3132-118">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3132-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3132-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3132-119">INPUTS</span></span>

### <span data-ttu-id="f3132-120">Нет</span><span class="sxs-lookup"><span data-stu-id="f3132-120">None</span></span>

## <span data-ttu-id="f3132-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3132-121">OUTPUTS</span></span>

### <span data-ttu-id="f3132-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="f3132-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="f3132-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3132-123">NOTES</span></span>
<span data-ttu-id="f3132-124">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f3132-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f3132-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3132-125">RELATED LINKS</span></span>
