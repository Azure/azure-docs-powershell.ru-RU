---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/import-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: b54e7cf5af7eadd0ea56687a336175650b55daa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564348"
---
# <span data-ttu-id="325dd-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="325dd-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="325dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="325dd-102">SYNOPSIS</span></span>
<span data-ttu-id="325dd-103">Импортирует объект JSON в определение веб-службы.</span><span class="sxs-lookup"><span data-stu-id="325dd-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="325dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="325dd-104">SYNTAX</span></span>

### <span data-ttu-id="325dd-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="325dd-105">ImportFromJSONFile</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="325dd-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="325dd-106">ImportFromJSONString.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="325dd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="325dd-107">DESCRIPTION</span></span>
<span data-ttu-id="325dd-108">Командлет Import-AzureRmMlWebService импортирует, задается непосредственно или в файле, на который указывает ссылка, и создает объект определения веб-службы, который можно передать в командлет New-AzureRmMlWebService.</span><span class="sxs-lookup"><span data-stu-id="325dd-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="325dd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="325dd-109">EXAMPLES</span></span>

### <span data-ttu-id="325dd-110">Пример 1: импорт из строки</span><span class="sxs-lookup"><span data-stu-id="325dd-110">Example 1: Import from string</span></span>
```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="325dd-111">Пример 2: импорт из пути к файлу</span><span class="sxs-lookup"><span data-stu-id="325dd-111">Example 2: Import from file path</span></span>
```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="325dd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="325dd-112">PARAMETERS</span></span>

### <span data-ttu-id="325dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325dd-113">-DefaultProfile</span></span>
<span data-ttu-id="325dd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="325dd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="325dd-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="325dd-115">-InputFile</span></span>
<span data-ttu-id="325dd-116">Путь к файлу, содержащему определение веб-службы, которое нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="325dd-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325dd-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="325dd-117">-JsonString</span></span>
<span data-ttu-id="325dd-118">Отформатированная строка JSON, содержащая определение веб-службы для импорта.</span><span class="sxs-lookup"><span data-stu-id="325dd-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325dd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325dd-119">CommonParameters</span></span>
<span data-ttu-id="325dd-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="325dd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325dd-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="325dd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325dd-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="325dd-122">INPUTS</span></span>

### <span data-ttu-id="325dd-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="325dd-123">None</span></span>

## <span data-ttu-id="325dd-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="325dd-124">OUTPUTS</span></span>

### <span data-ttu-id="325dd-125">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="325dd-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="325dd-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="325dd-126">NOTES</span></span>
<span data-ttu-id="325dd-127">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="325dd-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="325dd-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="325dd-128">RELATED LINKS</span></span>
