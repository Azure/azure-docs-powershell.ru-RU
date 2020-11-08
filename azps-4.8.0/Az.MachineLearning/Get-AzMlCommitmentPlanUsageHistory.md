---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236139"
---
# <span data-ttu-id="5ccdc-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="5ccdc-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="5ccdc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ccdc-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccdc-103">Извлекает сведения о журнале использования для указанного плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="5ccdc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ccdc-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ccdc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ccdc-105">DESCRIPTION</span></span>
<span data-ttu-id="5ccdc-106">Получение сведений об использовании для определенного плана обязательства, включая используемые ресурсы и ресурсы, остающиеся в плане.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="5ccdc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ccdc-107">EXAMPLES</span></span>

### <span data-ttu-id="5ccdc-108">Пример 1: получение журнала использования для определенного плана обязательства</span><span class="sxs-lookup"><span data-stu-id="5ccdc-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="5ccdc-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ccdc-109">PARAMETERS</span></span>

### <span data-ttu-id="5ccdc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ccdc-110">-DefaultProfile</span></span>
<span data-ttu-id="5ccdc-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ccdc-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ccdc-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5ccdc-112">-Name</span></span>
<span data-ttu-id="5ccdc-113">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="5ccdc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ccdc-114">-ResourceGroupName</span></span>
<span data-ttu-id="5ccdc-115">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="5ccdc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccdc-116">CommonParameters</span></span>
<span data-ttu-id="5ccdc-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccdc-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ccdc-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccdc-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ccdc-119">INPUTS</span></span>

### <span data-ttu-id="5ccdc-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="5ccdc-120">None</span></span>

## <span data-ttu-id="5ccdc-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ccdc-121">OUTPUTS</span></span>

### <span data-ttu-id="5ccdc-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="5ccdc-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="5ccdc-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ccdc-123">NOTES</span></span>
<span data-ttu-id="5ccdc-124">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5ccdc-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5ccdc-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ccdc-125">RELATED LINKS</span></span>
