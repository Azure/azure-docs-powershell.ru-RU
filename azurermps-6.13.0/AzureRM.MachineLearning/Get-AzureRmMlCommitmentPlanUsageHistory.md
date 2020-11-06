---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 481d1e26ad769101f06acda5573175bd06331fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569840"
---
# <span data-ttu-id="3fdfa-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="3fdfa-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="3fdfa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3fdfa-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdfa-103">Извлекает сведения о журнале использования для указанного плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fdfa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3fdfa-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fdfa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fdfa-105">DESCRIPTION</span></span>
<span data-ttu-id="3fdfa-106">Получение сведений об использовании для определенного плана обязательства, включая используемые ресурсы и ресурсы, остающиеся в плане.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="3fdfa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3fdfa-107">EXAMPLES</span></span>

### <span data-ttu-id="3fdfa-108">Пример 1: получение журнала использования для определенного плана обязательства</span><span class="sxs-lookup"><span data-stu-id="3fdfa-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="3fdfa-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3fdfa-109">PARAMETERS</span></span>

### <span data-ttu-id="3fdfa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fdfa-110">-DefaultProfile</span></span>
<span data-ttu-id="3fdfa-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3fdfa-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fdfa-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3fdfa-112">-Name</span></span>
<span data-ttu-id="3fdfa-113">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3fdfa-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fdfa-114">-ResourceGroupName</span></span>
<span data-ttu-id="3fdfa-115">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3fdfa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdfa-116">CommonParameters</span></span>
<span data-ttu-id="3fdfa-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3fdfa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdfa-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fdfa-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdfa-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3fdfa-119">INPUTS</span></span>

### <span data-ttu-id="3fdfa-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="3fdfa-120">None</span></span>

## <span data-ttu-id="3fdfa-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fdfa-121">OUTPUTS</span></span>

### <span data-ttu-id="3fdfa-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="3fdfa-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="3fdfa-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="3fdfa-123">NOTES</span></span>
<span data-ttu-id="3fdfa-124">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3fdfa-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3fdfa-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fdfa-125">RELATED LINKS</span></span>
