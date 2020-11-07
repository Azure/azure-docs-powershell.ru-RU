---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: a7e784d312ea834e30dac2243aefd880dca09dd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720447"
---
# <span data-ttu-id="e5e6c-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="e5e6c-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="e5e6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e6c-103">Извлекает ключи веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e5e6c-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="e5e6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5e6c-104">SYNTAX</span></span>

### <span data-ttu-id="e5e6c-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5e6c-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5e6c-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="e5e6c-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5e6c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5e6c-107">DESCRIPTION</span></span>
<span data-ttu-id="e5e6c-108">Возвращает клавиши доступа для API среды выполнения веб-службы машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e6c-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="e5e6c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5e6c-109">EXAMPLES</span></span>

### <span data-ttu-id="e5e6c-110">Пример 1: получение ключей для веб-службы, заданной группой ресурсов и именем</span><span class="sxs-lookup"><span data-stu-id="e5e6c-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="e5e6c-111">Пример 2: получение ключей для экземпляра веб-службы</span><span class="sxs-lookup"><span data-stu-id="e5e6c-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="e5e6c-112">$mlService является объектом типа Microsoft. Azure. Management. MachineLearning. WebService. WebService.</span><span class="sxs-lookup"><span data-stu-id="e5e6c-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="e5e6c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5e6c-113">PARAMETERS</span></span>

### <span data-ttu-id="e5e6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e6c-114">-DefaultProfile</span></span>
<span data-ttu-id="e5e6c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e5e6c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5e6c-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="e5e6c-116">-MlWebService</span></span>
<span data-ttu-id="e5e6c-117">Имя веб-службы, для которой извлекаются клавиши доступа.</span><span class="sxs-lookup"><span data-stu-id="e5e6c-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="e5e6c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5e6c-118">-Name</span></span>
<span data-ttu-id="e5e6c-119">Имя веб-службы, для которой извлекаются клавиши доступа.</span><span class="sxs-lookup"><span data-stu-id="e5e6c-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="e5e6c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e6c-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5e6c-121">Группа ресурсов для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e5e6c-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="e5e6c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e6c-122">CommonParameters</span></span>
<span data-ttu-id="e5e6c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5e6c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e6c-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e6c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e6c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5e6c-125">INPUTS</span></span>

### <span data-ttu-id="e5e6c-126">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="e5e6c-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e5e6c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5e6c-127">OUTPUTS</span></span>

### <span data-ttu-id="e5e6c-128">Microsoft. Azure. Management. MachineLearning. WebService. Models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="e5e6c-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="e5e6c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5e6c-129">NOTES</span></span>
<span data-ttu-id="e5e6c-130">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e5e6c-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e5e6c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5e6c-131">RELATED LINKS</span></span>
