---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/import-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: cc6c596b028ca7a4b89083ff06d37b3df9c3ed7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565508"
---
# <span data-ttu-id="1771d-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="1771d-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="1771d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1771d-102">SYNOPSIS</span></span>
<span data-ttu-id="1771d-103">Импортирует объект JSON в определение веб-службы.</span><span class="sxs-lookup"><span data-stu-id="1771d-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1771d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1771d-104">SYNTAX</span></span>

### <span data-ttu-id="1771d-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="1771d-105">ImportFromJSONFile</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1771d-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="1771d-106">ImportFromJSONString.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1771d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1771d-107">DESCRIPTION</span></span>
<span data-ttu-id="1771d-108">Командлет Import-AzureRmMlWebService импортирует, задается непосредственно или в файле, на который указывает ссылка, и создает объект определения веб-службы, который можно передать в командлет New-AzureRmMlWebService.</span><span class="sxs-lookup"><span data-stu-id="1771d-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="1771d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1771d-109">EXAMPLES</span></span>

### <span data-ttu-id="1771d-110">--------------------------Пример 1: импорт из строки--------------------------</span><span class="sxs-lookup"><span data-stu-id="1771d-110">--------------------------  Example 1: Import from string  --------------------------</span></span>
```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="1771d-111">--------------------------Пример 2: импорт из пути к файлу--------------------------</span><span class="sxs-lookup"><span data-stu-id="1771d-111">--------------------------  Example 2: Import from file path  --------------------------</span></span>
```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="1771d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1771d-112">PARAMETERS</span></span>

### <span data-ttu-id="1771d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1771d-113">-DefaultProfile</span></span>
<span data-ttu-id="1771d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1771d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1771d-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="1771d-115">-InputFile</span></span>
<span data-ttu-id="1771d-116">Путь к файлу, содержащему определение веб-службы, которое нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="1771d-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromJSONFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1771d-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="1771d-117">-JsonString</span></span>
<span data-ttu-id="1771d-118">Отформатированная строка JSON, содержащая определение веб-службы для импорта.</span><span class="sxs-lookup"><span data-stu-id="1771d-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromJSONString.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1771d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1771d-119">CommonParameters</span></span>
<span data-ttu-id="1771d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1771d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1771d-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1771d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1771d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1771d-122">INPUTS</span></span>

### <span data-ttu-id="1771d-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="1771d-123">None</span></span>
<span data-ttu-id="1771d-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1771d-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1771d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1771d-125">OUTPUTS</span></span>

### <span data-ttu-id="1771d-126">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="1771d-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="1771d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="1771d-127">NOTES</span></span>
<span data-ttu-id="1771d-128">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="1771d-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1771d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1771d-129">RELATED LINKS</span></span>

