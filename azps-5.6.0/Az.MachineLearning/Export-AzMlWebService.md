---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 0fad6a81f895643f8783ca8d179d68e31eed6da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976792"
---
# <span data-ttu-id="91f89-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="91f89-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="91f89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91f89-102">SYNOPSIS</span></span>
<span data-ttu-id="91f89-103">Экспорт объекта определения веб-службы в виде строки в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="91f89-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="91f89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91f89-104">SYNTAX</span></span>

### <span data-ttu-id="91f89-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="91f89-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91f89-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="91f89-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91f89-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91f89-107">DESCRIPTION</span></span>
<span data-ttu-id="91f89-108">Экспорт объекта определения для указанной веб-службы в виде строки в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="91f89-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="91f89-109">Вы можете сразу же вернуть строку или сохранить ее в файл.</span><span class="sxs-lookup"><span data-stu-id="91f89-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="91f89-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91f89-110">EXAMPLES</span></span>

### <span data-ttu-id="91f89-111">Пример 1. Экспорт в строку</span><span class="sxs-lookup"><span data-stu-id="91f89-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="91f89-112">Пример 2. Экспорт в файл</span><span class="sxs-lookup"><span data-stu-id="91f89-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="91f89-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91f89-113">PARAMETERS</span></span>

### <span data-ttu-id="91f89-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f89-114">-DefaultProfile</span></span>
<span data-ttu-id="91f89-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="91f89-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91f89-116">-Force</span><span class="sxs-lookup"><span data-stu-id="91f89-116">-Force</span></span>
<span data-ttu-id="91f89-117">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="91f89-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="91f89-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="91f89-118">-OutputFile</span></span>
<span data-ttu-id="91f89-119">Путь к файлу для экспортируемой определения.</span><span class="sxs-lookup"><span data-stu-id="91f89-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="91f89-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="91f89-120">-ToJsonString</span></span>
<span data-ttu-id="91f89-121">Указывает, что определение будет экспортироваться как строка JSON.</span><span class="sxs-lookup"><span data-stu-id="91f89-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="91f89-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="91f89-122">-WebService</span></span>
<span data-ttu-id="91f89-123">Объект определения веб-службы, который нужно экспортировать.</span><span class="sxs-lookup"><span data-stu-id="91f89-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="91f89-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91f89-124">-Confirm</span></span>
<span data-ttu-id="91f89-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91f89-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f89-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f89-126">-WhatIf</span></span>
<span data-ttu-id="91f89-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91f89-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91f89-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="91f89-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f89-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f89-129">CommonParameters</span></span>
<span data-ttu-id="91f89-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f89-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f89-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91f89-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f89-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91f89-132">INPUTS</span></span>

### <span data-ttu-id="91f89-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="91f89-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="91f89-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91f89-134">OUTPUTS</span></span>

### <span data-ttu-id="91f89-135">System.String</span><span class="sxs-lookup"><span data-stu-id="91f89-135">System.String</span></span>

## <span data-ttu-id="91f89-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91f89-136">NOTES</span></span>
<span data-ttu-id="91f89-137">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="91f89-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="91f89-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91f89-138">RELATED LINKS</span></span>
