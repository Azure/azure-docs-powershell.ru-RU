---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248936"
---
# <span data-ttu-id="7770a-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="7770a-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="7770a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7770a-102">SYNOPSIS</span></span>
<span data-ttu-id="7770a-103">Извлекает ключи веб-службы.</span><span class="sxs-lookup"><span data-stu-id="7770a-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="7770a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7770a-104">SYNTAX</span></span>

### <span data-ttu-id="7770a-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7770a-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7770a-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="7770a-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7770a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7770a-107">DESCRIPTION</span></span>
<span data-ttu-id="7770a-108">Возвращает клавиши доступа для API среды выполнения веб-службы машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="7770a-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="7770a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7770a-109">EXAMPLES</span></span>

### <span data-ttu-id="7770a-110">Пример 1: получение ключей для веб-службы, заданной группой ресурсов и именем</span><span class="sxs-lookup"><span data-stu-id="7770a-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="7770a-111">Пример 2: получение ключей для экземпляра веб-службы</span><span class="sxs-lookup"><span data-stu-id="7770a-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="7770a-112">$mlService является объектом типа Microsoft. Azure. Management. MachineLearning. WebService. WebService.</span><span class="sxs-lookup"><span data-stu-id="7770a-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="7770a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7770a-113">PARAMETERS</span></span>

### <span data-ttu-id="7770a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7770a-114">-DefaultProfile</span></span>
<span data-ttu-id="7770a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7770a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7770a-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="7770a-116">-MlWebService</span></span>
<span data-ttu-id="7770a-117">Имя веб-службы, для которой извлекаются клавиши доступа.</span><span class="sxs-lookup"><span data-stu-id="7770a-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7770a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7770a-118">-Name</span></span>
<span data-ttu-id="7770a-119">Имя веб-службы, для которой извлекаются клавиши доступа.</span><span class="sxs-lookup"><span data-stu-id="7770a-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7770a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7770a-120">-ResourceGroupName</span></span>
<span data-ttu-id="7770a-121">Группа ресурсов для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="7770a-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7770a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7770a-122">CommonParameters</span></span>
<span data-ttu-id="7770a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7770a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7770a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7770a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7770a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7770a-125">INPUTS</span></span>

### <span data-ttu-id="7770a-126">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="7770a-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7770a-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7770a-127">OUTPUTS</span></span>

### <span data-ttu-id="7770a-128">Microsoft. Azure. Management. MachineLearning. WebService. Models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="7770a-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="7770a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="7770a-129">NOTES</span></span>
<span data-ttu-id="7770a-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7770a-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7770a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7770a-131">RELATED LINKS</span></span>