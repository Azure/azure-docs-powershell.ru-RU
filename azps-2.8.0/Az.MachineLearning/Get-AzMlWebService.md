---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: 73e20db774e6df70086eef6dc61a2ba9ecfb8689
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720446"
---
# <span data-ttu-id="432b5-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="432b5-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="432b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="432b5-102">SYNOPSIS</span></span>
<span data-ttu-id="432b5-103">Извлекает сводные данные для одной или нескольких веб-служб.</span><span class="sxs-lookup"><span data-stu-id="432b5-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="432b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="432b5-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="432b5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="432b5-105">DESCRIPTION</span></span>
<span data-ttu-id="432b5-106">Получение сведений об определении веб-службы.</span><span class="sxs-lookup"><span data-stu-id="432b5-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="432b5-107">В зависимости от переданных параметров командлет возвращает определение определенной веб-службы, коллекцию определений для веб-служб для указанной группы ресурсов в текущей подписке или коллекцию определений для веб-служб в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="432b5-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="432b5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="432b5-108">EXAMPLES</span></span>

### <span data-ttu-id="432b5-109">Пример 1: получение подробных сведений о конкретной веб-службе</span><span class="sxs-lookup"><span data-stu-id="432b5-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="432b5-110">Пример 2: получение всех ресурсов веб-службы в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="432b5-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="432b5-111">Пример 3: получение всех веб-служб в текущей подписке и данной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="432b5-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="432b5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="432b5-112">PARAMETERS</span></span>

### <span data-ttu-id="432b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="432b5-113">-DefaultProfile</span></span>
<span data-ttu-id="432b5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="432b5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="432b5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="432b5-115">-Name</span></span>
<span data-ttu-id="432b5-116">Имя веб-службы, сведения о которой извлекаются.</span><span class="sxs-lookup"><span data-stu-id="432b5-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="432b5-117">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="432b5-117">-Region</span></span>
<span data-ttu-id="432b5-118">Имя региона</span><span class="sxs-lookup"><span data-stu-id="432b5-118">The name of region</span></span>

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

### <span data-ttu-id="432b5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="432b5-119">-ResourceGroupName</span></span>
<span data-ttu-id="432b5-120">Группа ресурсов, из которой извлекаются сведения о веб-службе.</span><span class="sxs-lookup"><span data-stu-id="432b5-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="432b5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="432b5-121">CommonParameters</span></span>
<span data-ttu-id="432b5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="432b5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="432b5-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="432b5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="432b5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="432b5-124">INPUTS</span></span>

### <span data-ttu-id="432b5-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="432b5-125">None</span></span>

## <span data-ttu-id="432b5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="432b5-126">OUTPUTS</span></span>

### <span data-ttu-id="432b5-127">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="432b5-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="432b5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="432b5-128">NOTES</span></span>
<span data-ttu-id="432b5-129">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="432b5-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="432b5-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="432b5-130">RELATED LINKS</span></span>
