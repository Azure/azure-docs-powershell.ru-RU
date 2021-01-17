---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415516"
---
# <span data-ttu-id="8497e-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="8497e-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="8497e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8497e-102">SYNOPSIS</span></span>
<span data-ttu-id="8497e-103">Извлекает сводную информацию для одной или двух веб-служб.</span><span class="sxs-lookup"><span data-stu-id="8497e-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="8497e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8497e-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8497e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8497e-105">DESCRIPTION</span></span>
<span data-ttu-id="8497e-106">Извлекает сведения определения веб-службы.</span><span class="sxs-lookup"><span data-stu-id="8497e-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="8497e-107">В зависимости от переданных параметров он возвращает определение определенной веб-службы, набор определений веб-служб для указанной группы ресурсов в текущей подписке или набор определений для веб-служб в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8497e-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="8497e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8497e-108">EXAMPLES</span></span>

### <span data-ttu-id="8497e-109">Пример 1. Подробные сведения об определенной веб-службе</span><span class="sxs-lookup"><span data-stu-id="8497e-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="8497e-110">Пример 2. Получить все ресурсы веб-служб в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="8497e-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="8497e-111">Пример 3. Получить все веб-службы в текущей подписке и предоставленную группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="8497e-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="8497e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8497e-112">PARAMETERS</span></span>

### <span data-ttu-id="8497e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8497e-113">-DefaultProfile</span></span>
<span data-ttu-id="8497e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8497e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8497e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8497e-115">-Name</span></span>
<span data-ttu-id="8497e-116">Имя веб-службы, сведения о которой извлекаются.</span><span class="sxs-lookup"><span data-stu-id="8497e-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="8497e-117">-Регион</span><span class="sxs-lookup"><span data-stu-id="8497e-117">-Region</span></span>
<span data-ttu-id="8497e-118">Название региона</span><span class="sxs-lookup"><span data-stu-id="8497e-118">The name of region</span></span>

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

### <span data-ttu-id="8497e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8497e-119">-ResourceGroupName</span></span>
<span data-ttu-id="8497e-120">Группа ресурсов, сведения о которой извлекаются из веб-службы.</span><span class="sxs-lookup"><span data-stu-id="8497e-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="8497e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8497e-121">CommonParameters</span></span>
<span data-ttu-id="8497e-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8497e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8497e-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8497e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8497e-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8497e-124">INPUTS</span></span>

### <span data-ttu-id="8497e-125">Нет</span><span class="sxs-lookup"><span data-stu-id="8497e-125">None</span></span>

## <span data-ttu-id="8497e-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8497e-126">OUTPUTS</span></span>

### <span data-ttu-id="8497e-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="8497e-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="8497e-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8497e-128">NOTES</span></span>
<span data-ttu-id="8497e-129">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="8497e-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="8497e-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8497e-130">RELATED LINKS</span></span>
