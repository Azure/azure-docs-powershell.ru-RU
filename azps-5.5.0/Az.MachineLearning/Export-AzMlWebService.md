---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241357"
---
# <span data-ttu-id="7f2b5-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="7f2b5-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="7f2b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f2b5-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2b5-103">Экспорт объекта определения веб-службы в виде строки в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="7f2b5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f2b5-104">SYNTAX</span></span>

### <span data-ttu-id="7f2b5-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="7f2b5-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f2b5-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="7f2b5-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f2b5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f2b5-107">DESCRIPTION</span></span>
<span data-ttu-id="7f2b5-108">Экспорт объекта определения для указанной веб-службы в виде строки в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="7f2b5-109">Вы можете сразу же вернуть строку или сохранить ее в файл.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="7f2b5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f2b5-110">EXAMPLES</span></span>

### <span data-ttu-id="7f2b5-111">Пример 1. Экспорт в качестве строки</span><span class="sxs-lookup"><span data-stu-id="7f2b5-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="7f2b5-112">Пример 2. Экспорт в файл</span><span class="sxs-lookup"><span data-stu-id="7f2b5-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="7f2b5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f2b5-113">PARAMETERS</span></span>

### <span data-ttu-id="7f2b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2b5-114">-DefaultProfile</span></span>
<span data-ttu-id="7f2b5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7f2b5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f2b5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7f2b5-116">-Force</span></span>
<span data-ttu-id="7f2b5-117">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b5-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="7f2b5-118">-OutputFile</span></span>
<span data-ttu-id="7f2b5-119">Путь к файлу для экспортируемой определения.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b5-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="7f2b5-120">-ToJsonString</span></span>
<span data-ttu-id="7f2b5-121">Указывает, что определение будет экспортироваться как строка JSON.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b5-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="7f2b5-122">-WebService</span></span>
<span data-ttu-id="7f2b5-123">Объект определения веб-службы, который нужно экспортировать.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f2b5-124">-Confirm</span></span>
<span data-ttu-id="7f2b5-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f2b5-126">-WhatIf</span></span>
<span data-ttu-id="7f2b5-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f2b5-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2b5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2b5-129">CommonParameters</span></span>
<span data-ttu-id="7f2b5-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f2b5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2b5-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f2b5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2b5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f2b5-132">INPUTS</span></span>

### <span data-ttu-id="7f2b5-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="7f2b5-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7f2b5-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f2b5-134">OUTPUTS</span></span>

### <span data-ttu-id="7f2b5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7f2b5-135">System.String</span></span>

## <span data-ttu-id="7f2b5-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f2b5-136">NOTES</span></span>
<span data-ttu-id="7f2b5-137">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7f2b5-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7f2b5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f2b5-138">RELATED LINKS</span></span>
