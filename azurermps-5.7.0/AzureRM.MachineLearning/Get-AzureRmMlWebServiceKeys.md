---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: a0019b418fbf71a9b8010b4256a062a943244a9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565509"
---
# <span data-ttu-id="f51cd-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="f51cd-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="f51cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f51cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f51cd-103">Извлекает ключи веб-службы.</span><span class="sxs-lookup"><span data-stu-id="f51cd-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f51cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f51cd-104">SYNTAX</span></span>

### <span data-ttu-id="f51cd-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f51cd-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f51cd-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="f51cd-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f51cd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f51cd-107">DESCRIPTION</span></span>
<span data-ttu-id="f51cd-108">Возвращает клавиши доступа для API среды выполнения веб-службы машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="f51cd-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="f51cd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f51cd-109">EXAMPLES</span></span>

### <span data-ttu-id="f51cd-110">--------------------------Примере 1 — получение ключей для веб-службы, заданной группой ресурсов и именем--------------------------</span><span class="sxs-lookup"><span data-stu-id="f51cd-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="f51cd-111">--------------------------Пример 2 — получение ключей для экземпляра веб-службы--------------------------</span><span class="sxs-lookup"><span data-stu-id="f51cd-111">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="f51cd-112">$mlService является объектом типа Microsoft. Azure. Management. MachineLearning. WebService. WebService.</span><span class="sxs-lookup"><span data-stu-id="f51cd-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="f51cd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f51cd-113">PARAMETERS</span></span>

### <span data-ttu-id="f51cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f51cd-114">-DefaultProfile</span></span>
<span data-ttu-id="f51cd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f51cd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f51cd-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="f51cd-116">-MlWebService</span></span>
<span data-ttu-id="f51cd-117">Имя веб-службы, для которой извлекаются клавиши доступа.</span><span class="sxs-lookup"><span data-stu-id="f51cd-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: WebService
Parameter Sets: GetByInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f51cd-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f51cd-118">-Name</span></span>
<span data-ttu-id="f51cd-119">Имя веб-службы, для которой извлекаются клавиши доступа.</span><span class="sxs-lookup"><span data-stu-id="f51cd-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51cd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f51cd-120">-ResourceGroupName</span></span>
<span data-ttu-id="f51cd-121">Группа ресурсов для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="f51cd-121">The resource group for the web service.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f51cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f51cd-122">CommonParameters</span></span>
<span data-ttu-id="f51cd-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f51cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f51cd-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f51cd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f51cd-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f51cd-125">INPUTS</span></span>

### <span data-ttu-id="f51cd-126">Вебслужба</span><span class="sxs-lookup"><span data-stu-id="f51cd-126">WebService</span></span>
<span data-ttu-id="f51cd-127">Параметр "MlWebService" принимает значение типа WebService из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f51cd-127">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="f51cd-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f51cd-128">OUTPUTS</span></span>

### <span data-ttu-id="f51cd-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="f51cd-129">None</span></span>

## <span data-ttu-id="f51cd-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f51cd-130">NOTES</span></span>
<span data-ttu-id="f51cd-131">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f51cd-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f51cd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f51cd-132">RELATED LINKS</span></span>

