---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569367"
---
# <span data-ttu-id="d547c-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="d547c-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="d547c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d547c-102">SYNOPSIS</span></span>
<span data-ttu-id="d547c-103">Извлекает ключи веб-службы.</span><span class="sxs-lookup"><span data-stu-id="d547c-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d547c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d547c-104">SYNTAX</span></span>

### <span data-ttu-id="d547c-105">Получение ключей доступа для веб-службы Azure ML по имени и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d547c-105">Get an Azure ML web service's access keys given its name and resource group.</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d547c-106">Получение kesy доступа для заданного экземпляра веб-службы.</span><span class="sxs-lookup"><span data-stu-id="d547c-106">Get the access kesy for the given web service instance.</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d547c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d547c-107">DESCRIPTION</span></span>
<span data-ttu-id="d547c-108">Возвращает клавиши доступа для API среды выполнения веб-службы машинного обучения Azure.</span><span class="sxs-lookup"><span data-stu-id="d547c-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="d547c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d547c-109">EXAMPLES</span></span>

### <span data-ttu-id="d547c-110">--------------------------Примере 1 — получение ключей для веб-службы, заданной группой ресурсов и именем--------------------------</span><span class="sxs-lookup"><span data-stu-id="d547c-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
<span data-ttu-id="d547c-111">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d547c-111">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="d547c-112">--------------------------Пример 2 — получение ключей для экземпляра веб-службы--------------------------</span><span class="sxs-lookup"><span data-stu-id="d547c-112">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
<span data-ttu-id="d547c-113">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d547c-113">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="d547c-114">$mlService является объектом типа Microsoft. Azure. Management. MachineLearning. WebService. WebService.</span><span class="sxs-lookup"><span data-stu-id="d547c-114">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="d547c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d547c-115">PARAMETERS</span></span>

### <span data-ttu-id="d547c-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="d547c-116">-MlWebService</span></span>
<span data-ttu-id="d547c-117">Имя веб-службы, для которой извлекаются клавиши доступа.</span><span class="sxs-lookup"><span data-stu-id="d547c-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d547c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d547c-118">-Name</span></span>
<span data-ttu-id="d547c-119">Имя веб-службы, для которой извлекаются клавиши доступа.</span><span class="sxs-lookup"><span data-stu-id="d547c-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d547c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d547c-120">-ResourceGroupName</span></span>
<span data-ttu-id="d547c-121">Группа ресурсов для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="d547c-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d547c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d547c-122">-DefaultProfile</span></span>
<span data-ttu-id="d547c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d547c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d547c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d547c-124">CommonParameters</span></span>
<span data-ttu-id="d547c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d547c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d547c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d547c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d547c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d547c-127">INPUTS</span></span>

### <span data-ttu-id="d547c-128">Вебслужба</span><span class="sxs-lookup"><span data-stu-id="d547c-128">WebService</span></span>
<span data-ttu-id="d547c-129">Параметр "MlWebService" принимает значение типа WebService из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d547c-129">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="d547c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d547c-130">OUTPUTS</span></span>

### <span data-ttu-id="d547c-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="d547c-131">None</span></span>

## <span data-ttu-id="d547c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d547c-132">NOTES</span></span>
<span data-ttu-id="d547c-133">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d547c-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d547c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d547c-134">RELATED LINKS</span></span>

