---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 802a3be7aca857b798f1e853bec499c5397b6e65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561732"
---
# <span data-ttu-id="b61b0-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="b61b0-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="b61b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b61b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b61b0-103">Извлекает сводные данные для одной или нескольких веб-служб.</span><span class="sxs-lookup"><span data-stu-id="b61b0-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b61b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b61b0-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b61b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b61b0-105">DESCRIPTION</span></span>
<span data-ttu-id="b61b0-106">Извлекает сведения определения веб-службы.</span><span class="sxs-lookup"><span data-stu-id="b61b0-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="b61b0-107">В зависимости от параметров, которые передавались, командлет возвращает определения для определенной веб-службы, коллекцию defintions для веб-служб для указанной группы ресурсов в текущей подписке или коллекцию defintions для веб-служб в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b61b0-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="b61b0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b61b0-108">EXAMPLES</span></span>

### <span data-ttu-id="b61b0-109">--------------------------Пример 1: получение подробных сведений об определенных веб-службах--------------------------</span><span class="sxs-lookup"><span data-stu-id="b61b0-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="b61b0-110">--------------------------Пример 2: получение всех ресурсов веб-службы в текущей подписке--------------------------</span><span class="sxs-lookup"><span data-stu-id="b61b0-110">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
```
Get-AzureRmMlWebService
```

### <span data-ttu-id="b61b0-111">--------------------------Пример 3: получение всех веб-служб в текущей подписке и данной группе ресурсов--------------------------</span><span class="sxs-lookup"><span data-stu-id="b61b0-111">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="b61b0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b61b0-112">PARAMETERS</span></span>

### <span data-ttu-id="b61b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61b0-113">-DefaultProfile</span></span>
<span data-ttu-id="b61b0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b61b0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b61b0-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b61b0-115">-Name</span></span>
<span data-ttu-id="b61b0-116">Имя веб-службы, сведения о которой извлекаются.</span><span class="sxs-lookup"><span data-stu-id="b61b0-116">The name of the web service for which the details are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61b0-117">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="b61b0-117">-Region</span></span>
<span data-ttu-id="b61b0-118">Имя Regio</span><span class="sxs-lookup"><span data-stu-id="b61b0-118">The name of regio</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61b0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b61b0-119">-ResourceGroupName</span></span>
<span data-ttu-id="b61b0-120">Группа ресурсов, из которой извлекаются сведения о веб-службе.</span><span class="sxs-lookup"><span data-stu-id="b61b0-120">The resource group from which the details for the web service are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61b0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61b0-121">CommonParameters</span></span>
<span data-ttu-id="b61b0-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b61b0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61b0-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b61b0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61b0-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b61b0-124">INPUTS</span></span>

### <span data-ttu-id="b61b0-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="b61b0-125">None</span></span>
<span data-ttu-id="b61b0-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b61b0-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b61b0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b61b0-127">OUTPUTS</span></span>

### <span data-ttu-id="b61b0-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="b61b0-128">None</span></span>

## <span data-ttu-id="b61b0-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b61b0-129">NOTES</span></span>
<span data-ttu-id="b61b0-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="b61b0-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b61b0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b61b0-131">RELATED LINKS</span></span>

