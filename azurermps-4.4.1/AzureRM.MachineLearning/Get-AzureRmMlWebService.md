---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569375"
---
# <span data-ttu-id="7bffd-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="7bffd-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="7bffd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7bffd-102">SYNOPSIS</span></span>
<span data-ttu-id="7bffd-103">Извлекает сводные данные для одной или нескольких веб-служб.</span><span class="sxs-lookup"><span data-stu-id="7bffd-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bffd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7bffd-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bffd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bffd-105">DESCRIPTION</span></span>
<span data-ttu-id="7bffd-106">Извлекает сведения определения веб-службы.</span><span class="sxs-lookup"><span data-stu-id="7bffd-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="7bffd-107">В зависимости от параметров, которые передавались, командлет возвращает определения для определенной веб-службы, коллекцию defintions для веб-служб для указанной группы ресурсов в текущей подписке или коллекцию defintions для веб-служб в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="7bffd-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="7bffd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7bffd-108">EXAMPLES</span></span>

### <span data-ttu-id="7bffd-109">--------------------------Пример 1: получение подробных сведений об определенных веб-службах--------------------------</span><span class="sxs-lookup"><span data-stu-id="7bffd-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
<span data-ttu-id="7bffd-110">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7bffd-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="7bffd-111">--------------------------Пример 2: получение всех ресурсов веб-службы в текущей подписке--------------------------</span><span class="sxs-lookup"><span data-stu-id="7bffd-111">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
<span data-ttu-id="7bffd-112">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7bffd-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService
```

### <span data-ttu-id="7bffd-113">--------------------------Пример 3: получение всех веб-служб в текущей подписке и данной группе ресурсов--------------------------</span><span class="sxs-lookup"><span data-stu-id="7bffd-113">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="7bffd-114">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7bffd-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="7bffd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7bffd-115">PARAMETERS</span></span>

### <span data-ttu-id="7bffd-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7bffd-116">-Name</span></span>
<span data-ttu-id="7bffd-117">Имя веб-службы, сведения о которой извлекаются.</span><span class="sxs-lookup"><span data-stu-id="7bffd-117">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="7bffd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bffd-118">-ResourceGroupName</span></span>
<span data-ttu-id="7bffd-119">Группа ресурсов, из которой извлекаются сведения о веб-службе.</span><span class="sxs-lookup"><span data-stu-id="7bffd-119">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="7bffd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bffd-120">-DefaultProfile</span></span>
<span data-ttu-id="7bffd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7bffd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bffd-122">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="7bffd-122">-Region</span></span>
<span data-ttu-id="7bffd-123">Имя региона</span><span class="sxs-lookup"><span data-stu-id="7bffd-123">The name of region</span></span>

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

### <span data-ttu-id="7bffd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bffd-124">CommonParameters</span></span>
<span data-ttu-id="7bffd-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7bffd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bffd-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bffd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bffd-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7bffd-127">INPUTS</span></span>

## <span data-ttu-id="7bffd-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bffd-128">OUTPUTS</span></span>

### <span data-ttu-id="7bffd-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="7bffd-129">None</span></span>

## <span data-ttu-id="7bffd-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7bffd-130">NOTES</span></span>
<span data-ttu-id="7bffd-131">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7bffd-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7bffd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bffd-132">RELATED LINKS</span></span>

