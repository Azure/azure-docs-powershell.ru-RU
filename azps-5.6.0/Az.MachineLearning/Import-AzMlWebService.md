---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: e30ecc151da5e4a202b8da63f8d57a8f25c387dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961875"
---
# <span data-ttu-id="87d3e-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="87d3e-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="87d3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="87d3e-103">Импорт объекта JSON в определение веб-службы.</span><span class="sxs-lookup"><span data-stu-id="87d3e-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="87d3e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="87d3e-104">SYNTAX</span></span>

### <span data-ttu-id="87d3e-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="87d3e-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87d3e-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="87d3e-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87d3e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87d3e-107">DESCRIPTION</span></span>
<span data-ttu-id="87d3e-108">С Import-AzMlWebService импортируется, задан непосредственно или в файле, на который указывает ссылка, и создается объект определения веб-службы, который можно передать New-AzMlWebService файлу.</span><span class="sxs-lookup"><span data-stu-id="87d3e-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="87d3e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="87d3e-109">EXAMPLES</span></span>

### <span data-ttu-id="87d3e-110">Пример 1. Импорт из строки</span><span class="sxs-lookup"><span data-stu-id="87d3e-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="87d3e-111">Пример 2. Импорт из пути к файлу</span><span class="sxs-lookup"><span data-stu-id="87d3e-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="87d3e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87d3e-112">PARAMETERS</span></span>

### <span data-ttu-id="87d3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d3e-113">-DefaultProfile</span></span>
<span data-ttu-id="87d3e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="87d3e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87d3e-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="87d3e-115">-InputFile</span></span>
<span data-ttu-id="87d3e-116">Путь к файлу, содержащего определение веб-службы для импорта.</span><span class="sxs-lookup"><span data-stu-id="87d3e-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="87d3e-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="87d3e-117">-JsonString</span></span>
<span data-ttu-id="87d3e-118">Строка в формате JSON, содержащая определение импортируемой веб-службы.</span><span class="sxs-lookup"><span data-stu-id="87d3e-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="87d3e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d3e-119">CommonParameters</span></span>
<span data-ttu-id="87d3e-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d3e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d3e-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87d3e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d3e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87d3e-122">INPUTS</span></span>

### <span data-ttu-id="87d3e-123">Нет</span><span class="sxs-lookup"><span data-stu-id="87d3e-123">None</span></span>

## <span data-ttu-id="87d3e-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87d3e-124">OUTPUTS</span></span>

### <span data-ttu-id="87d3e-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="87d3e-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="87d3e-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="87d3e-126">NOTES</span></span>
<span data-ttu-id="87d3e-127">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="87d3e-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="87d3e-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87d3e-128">RELATED LINKS</span></span>
