---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 5632de726797dd36af377f76b5919590c5826606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564359"
---
# <span data-ttu-id="5be6b-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="5be6b-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="5be6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5be6b-102">SYNOPSIS</span></span>
<span data-ttu-id="5be6b-103">Извлекает сводные данные для одной или нескольких веб-служб.</span><span class="sxs-lookup"><span data-stu-id="5be6b-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5be6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5be6b-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5be6b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5be6b-105">DESCRIPTION</span></span>
<span data-ttu-id="5be6b-106">Извлекает сведения определения веб-службы.</span><span class="sxs-lookup"><span data-stu-id="5be6b-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="5be6b-107">В зависимости от параметров, которые передавались, командлет возвращает определения для определенной веб-службы, коллекцию defintions для веб-служб для указанной группы ресурсов в текущей подписке или коллекцию defintions для веб-служб в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="5be6b-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="5be6b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5be6b-108">EXAMPLES</span></span>

### <span data-ttu-id="5be6b-109">Пример 1: получение подробных сведений о конкретной веб-службе</span><span class="sxs-lookup"><span data-stu-id="5be6b-109">Example 1: Get details of specific web service</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="5be6b-110">Пример 2: получение всех ресурсов веб-службы в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="5be6b-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzureRmMlWebService
```

### <span data-ttu-id="5be6b-111">Пример 3: получение всех веб-служб в текущей подписке и данной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5be6b-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="5be6b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5be6b-112">PARAMETERS</span></span>

### <span data-ttu-id="5be6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be6b-113">-DefaultProfile</span></span>
<span data-ttu-id="5be6b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5be6b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5be6b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5be6b-115">-Name</span></span>
<span data-ttu-id="5be6b-116">Имя веб-службы, сведения о которой извлекаются.</span><span class="sxs-lookup"><span data-stu-id="5be6b-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="5be6b-117">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="5be6b-117">-Region</span></span>
<span data-ttu-id="5be6b-118">Имя Regio</span><span class="sxs-lookup"><span data-stu-id="5be6b-118">The name of regio</span></span>

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

### <span data-ttu-id="5be6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5be6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="5be6b-120">Группа ресурсов, из которой извлекаются сведения о веб-службе.</span><span class="sxs-lookup"><span data-stu-id="5be6b-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="5be6b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be6b-121">CommonParameters</span></span>
<span data-ttu-id="5be6b-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5be6b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be6b-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5be6b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be6b-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5be6b-124">INPUTS</span></span>

### <span data-ttu-id="5be6b-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="5be6b-125">None</span></span>

## <span data-ttu-id="5be6b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5be6b-126">OUTPUTS</span></span>

### <span data-ttu-id="5be6b-127">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="5be6b-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="5be6b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="5be6b-128">NOTES</span></span>
<span data-ttu-id="5be6b-129">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5be6b-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5be6b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5be6b-130">RELATED LINKS</span></span>
