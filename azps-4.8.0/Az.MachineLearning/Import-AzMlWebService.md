---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 90416cd786e13bdd0232aebfcff2cd6963c1f872
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079960"
---
# <span data-ttu-id="e68e1-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="e68e1-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="e68e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e68e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e68e1-103">Импортирует объект JSON в определение веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e68e1-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="e68e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e68e1-104">SYNTAX</span></span>

### <span data-ttu-id="e68e1-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="e68e1-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e68e1-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="e68e1-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e68e1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e68e1-107">DESCRIPTION</span></span>
<span data-ttu-id="e68e1-108">Командлет Import-AzMlWebService импортирует, задается непосредственно или в файле, на который указывает ссылка, и создает объект определения веб-службы, который можно передать в командлет New-AzMlWebService.</span><span class="sxs-lookup"><span data-stu-id="e68e1-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="e68e1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e68e1-109">EXAMPLES</span></span>

### <span data-ttu-id="e68e1-110">Пример 1: импорт из строки</span><span class="sxs-lookup"><span data-stu-id="e68e1-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="e68e1-111">Пример 2: импорт из пути к файлу</span><span class="sxs-lookup"><span data-stu-id="e68e1-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="e68e1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e68e1-112">PARAMETERS</span></span>

### <span data-ttu-id="e68e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e68e1-113">-DefaultProfile</span></span>
<span data-ttu-id="e68e1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e68e1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e68e1-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e68e1-115">-InputFile</span></span>
<span data-ttu-id="e68e1-116">Путь к файлу, содержащему определение веб-службы, которое нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="e68e1-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="e68e1-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="e68e1-117">-JsonString</span></span>
<span data-ttu-id="e68e1-118">Отформатированная строка JSON, содержащая определение веб-службы для импорта.</span><span class="sxs-lookup"><span data-stu-id="e68e1-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="e68e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e68e1-119">CommonParameters</span></span>
<span data-ttu-id="e68e1-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e68e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e68e1-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e68e1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e68e1-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e68e1-122">INPUTS</span></span>

### <span data-ttu-id="e68e1-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="e68e1-123">None</span></span>

## <span data-ttu-id="e68e1-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e68e1-124">OUTPUTS</span></span>

### <span data-ttu-id="e68e1-125">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="e68e1-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e68e1-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e68e1-126">NOTES</span></span>
<span data-ttu-id="e68e1-127">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e68e1-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e68e1-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e68e1-128">RELATED LINKS</span></span>
