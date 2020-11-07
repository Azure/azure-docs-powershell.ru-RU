---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: e92f32dab72a4a96be03f800297194711f275d70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93735209"
---
# <span data-ttu-id="3d3e9-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="3d3e9-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="3d3e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d3e9-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3e9-103">Извлекает сведения о журнале использования для указанного плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d3e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d3e9-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d3e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d3e9-105">DESCRIPTION</span></span>
<span data-ttu-id="3d3e9-106">Получение сведений об использовании для определенного плана обязательства, включая используемые ресурсы и ресурсы, остающиеся в плане.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="3d3e9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d3e9-107">EXAMPLES</span></span>

### <span data-ttu-id="3d3e9-108">--------------------------Пример 1: получение журнала использования для определенного плана обязательства--------------------------</span><span class="sxs-lookup"><span data-stu-id="3d3e9-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="3d3e9-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d3e9-109">PARAMETERS</span></span>

### <span data-ttu-id="3d3e9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3e9-110">-DefaultProfile</span></span>
<span data-ttu-id="3d3e9-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3d3e9-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d3e9-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d3e9-112">-Name</span></span>
<span data-ttu-id="3d3e9-113">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3d3e9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d3e9-114">-ResourceGroupName</span></span>
<span data-ttu-id="3d3e9-115">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3d3e9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3e9-116">CommonParameters</span></span>
<span data-ttu-id="3d3e9-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3e9-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d3e9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3e9-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d3e9-119">INPUTS</span></span>

### <span data-ttu-id="3d3e9-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="3d3e9-120">None</span></span>
<span data-ttu-id="3d3e9-121">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3d3e9-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d3e9-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d3e9-122">OUTPUTS</span></span>

### <span data-ttu-id="3d3e9-123">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="3d3e9-123">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="3d3e9-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d3e9-124">NOTES</span></span>
<span data-ttu-id="3d3e9-125">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3d3e9-125">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3d3e9-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d3e9-126">RELATED LINKS</span></span>

