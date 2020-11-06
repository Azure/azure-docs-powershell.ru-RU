---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 9f9789d288773b16b2003e23b00674c12ca08738
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566708"
---
# <span data-ttu-id="1ea1e-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="1ea1e-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="1ea1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ea1e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea1e-103">Извлекает сводные данные по одному или нескольким планам обязательств.</span><span class="sxs-lookup"><span data-stu-id="1ea1e-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ea1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ea1e-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ea1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ea1e-105">DESCRIPTION</span></span>
<span data-ttu-id="1ea1e-106">Получение сведений о плане заобязанностей.</span><span class="sxs-lookup"><span data-stu-id="1ea1e-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="1ea1e-107">В зависимости от переданных параметров, командлет возвращает определенный план фиксации, набор планов фиксации для указанной группы ресурсов в текущей подписке или набор планов обязательства в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="1ea1e-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="1ea1e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ea1e-108">EXAMPLES</span></span>

### <span data-ttu-id="1ea1e-109">--------------------------Пример 1: получение плана для определенного обязательства--------------------------</span><span class="sxs-lookup"><span data-stu-id="1ea1e-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="1ea1e-110">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="1ea1e-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="1ea1e-111">--------------------------Пример 2: получение всех ресурсов плана обязательств в текущей подписке--------------------------</span><span class="sxs-lookup"><span data-stu-id="1ea1e-111">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
<span data-ttu-id="1ea1e-112">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="1ea1e-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="1ea1e-113">--------------------------Пример 3: получение всех планов обязательства в текущей подписке и данной группе ресурсов--------------------------</span><span class="sxs-lookup"><span data-stu-id="1ea1e-113">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="1ea1e-114">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="1ea1e-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="1ea1e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ea1e-115">PARAMETERS</span></span>

### <span data-ttu-id="1ea1e-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ea1e-116">-Name</span></span>
<span data-ttu-id="1ea1e-117">Название плана обязательства.</span><span class="sxs-lookup"><span data-stu-id="1ea1e-117">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="1ea1e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ea1e-118">-ResourceGroupName</span></span>
<span data-ttu-id="1ea1e-119">Имя группы ресурсов для плана фиксации Azure ML.</span><span class="sxs-lookup"><span data-stu-id="1ea1e-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="1ea1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea1e-120">-DefaultProfile</span></span>
<span data-ttu-id="1ea1e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ea1e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ea1e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea1e-122">CommonParameters</span></span>
<span data-ttu-id="1ea1e-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ea1e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea1e-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ea1e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea1e-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ea1e-125">INPUTS</span></span>

## <span data-ttu-id="1ea1e-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ea1e-126">OUTPUTS</span></span>

### <span data-ttu-id="1ea1e-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="1ea1e-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="1ea1e-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="1ea1e-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="1ea1e-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ea1e-129">NOTES</span></span>
<span data-ttu-id="1ea1e-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="1ea1e-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1ea1e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ea1e-131">RELATED LINKS</span></span>

