---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: c80278e460368ca6ec78efb4f5e74e456816df47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734825"
---
# <span data-ttu-id="10964-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="10964-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="10964-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10964-102">SYNOPSIS</span></span>
<span data-ttu-id="10964-103">Извлекает сведения о журнале использования для указанного плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="10964-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10964-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10964-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10964-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10964-105">DESCRIPTION</span></span>
<span data-ttu-id="10964-106">Получение сведений об использовании для определенного плана обязательства, включая используемые ресурсы и ресурсы, остающиеся в плане.</span><span class="sxs-lookup"><span data-stu-id="10964-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="10964-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10964-107">EXAMPLES</span></span>

### <span data-ttu-id="10964-108">--------------------------Пример 1: получение журнала использования для определенного плана обязательства--------------------------</span><span class="sxs-lookup"><span data-stu-id="10964-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="10964-109">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="10964-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="10964-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10964-110">PARAMETERS</span></span>

### <span data-ttu-id="10964-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="10964-111">-Name</span></span>
<span data-ttu-id="10964-112">Имя плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="10964-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="10964-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10964-113">-ResourceGroupName</span></span>
<span data-ttu-id="10964-114">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="10964-114">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="10964-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10964-115">-DefaultProfile</span></span>
<span data-ttu-id="10964-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10964-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10964-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10964-117">CommonParameters</span></span>
<span data-ttu-id="10964-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10964-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10964-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10964-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10964-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10964-120">INPUTS</span></span>

## <span data-ttu-id="10964-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10964-121">OUTPUTS</span></span>

### <span data-ttu-id="10964-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="10964-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="10964-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="10964-123">NOTES</span></span>
<span data-ttu-id="10964-124">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="10964-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="10964-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10964-125">RELATED LINKS</span></span>

