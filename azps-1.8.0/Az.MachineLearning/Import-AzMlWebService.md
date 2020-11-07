---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 7c885da5423e765cca3d18ce18957c0e64bb2c36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899765"
---
# <span data-ttu-id="7a465-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="7a465-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="7a465-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a465-102">SYNOPSIS</span></span>
<span data-ttu-id="7a465-103">Импортирует объект JSON в определение веб-службы.</span><span class="sxs-lookup"><span data-stu-id="7a465-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="7a465-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a465-104">SYNTAX</span></span>

### <span data-ttu-id="7a465-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="7a465-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a465-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="7a465-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a465-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a465-107">DESCRIPTION</span></span>
<span data-ttu-id="7a465-108">Командлет Import-AzMlWebService импортирует, задается непосредственно или в файле, на который указывает ссылка, и создает объект определения веб-службы, который можно передать в командлет New-AzMlWebService.</span><span class="sxs-lookup"><span data-stu-id="7a465-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="7a465-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a465-109">EXAMPLES</span></span>

### <span data-ttu-id="7a465-110">Пример 1: импорт из строки</span><span class="sxs-lookup"><span data-stu-id="7a465-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="7a465-111">Пример 2: импорт из пути к файлу</span><span class="sxs-lookup"><span data-stu-id="7a465-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="7a465-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a465-112">PARAMETERS</span></span>

### <span data-ttu-id="7a465-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a465-113">-DefaultProfile</span></span>
<span data-ttu-id="7a465-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7a465-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a465-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7a465-115">-InputFile</span></span>
<span data-ttu-id="7a465-116">Путь к файлу, содержащему определение веб-службы, которое нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="7a465-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="7a465-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="7a465-117">-JsonString</span></span>
<span data-ttu-id="7a465-118">Отформатированная строка JSON, содержащая определение веб-службы для импорта.</span><span class="sxs-lookup"><span data-stu-id="7a465-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="7a465-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a465-119">CommonParameters</span></span>
<span data-ttu-id="7a465-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a465-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a465-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a465-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a465-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a465-122">INPUTS</span></span>

### <span data-ttu-id="7a465-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="7a465-123">None</span></span>

## <span data-ttu-id="7a465-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a465-124">OUTPUTS</span></span>

### <span data-ttu-id="7a465-125">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="7a465-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7a465-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a465-126">NOTES</span></span>
<span data-ttu-id="7a465-127">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7a465-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7a465-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a465-128">RELATED LINKS</span></span>
