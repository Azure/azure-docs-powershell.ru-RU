---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072789"
---
# <span data-ttu-id="0cf8d-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="0cf8d-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="0cf8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0cf8d-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf8d-103">Экспортирует объект определения веб-службы в отформатированную строку в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="0cf8d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0cf8d-104">SYNTAX</span></span>

### <span data-ttu-id="0cf8d-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="0cf8d-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cf8d-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="0cf8d-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cf8d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cf8d-107">DESCRIPTION</span></span>
<span data-ttu-id="0cf8d-108">Экспортирует объект определения для указанной веб-службы в отформатированную строку JSON.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="0cf8d-109">Вы можете вернуть строку немедленно или сохранить ее в файле.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="0cf8d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0cf8d-110">EXAMPLES</span></span>

### <span data-ttu-id="0cf8d-111">Пример 1: экспорт в виде строки</span><span class="sxs-lookup"><span data-stu-id="0cf8d-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="0cf8d-112">Пример 2: экспорт в файл</span><span class="sxs-lookup"><span data-stu-id="0cf8d-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="0cf8d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0cf8d-113">PARAMETERS</span></span>

### <span data-ttu-id="0cf8d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf8d-114">-DefaultProfile</span></span>
<span data-ttu-id="0cf8d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0cf8d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cf8d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0cf8d-116">-Force</span></span>
<span data-ttu-id="0cf8d-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0cf8d-118">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="0cf8d-118">-OutputFile</span></span>
<span data-ttu-id="0cf8d-119">Путь к файлу для экспортированного определения.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="0cf8d-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="0cf8d-120">-ToJsonString</span></span>
<span data-ttu-id="0cf8d-121">Указывает, что определение будет экспортировано в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="0cf8d-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="0cf8d-122">-WebService</span></span>
<span data-ttu-id="0cf8d-123">Объект определения веб-службы, который необходимо экспортировать.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="0cf8d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cf8d-124">-Confirm</span></span>
<span data-ttu-id="0cf8d-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cf8d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cf8d-126">-WhatIf</span></span>
<span data-ttu-id="0cf8d-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cf8d-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cf8d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf8d-129">CommonParameters</span></span>
<span data-ttu-id="0cf8d-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf8d-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf8d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf8d-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0cf8d-132">INPUTS</span></span>

### <span data-ttu-id="0cf8d-133">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="0cf8d-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="0cf8d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cf8d-134">OUTPUTS</span></span>

### <span data-ttu-id="0cf8d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf8d-135">System.String</span></span>

## <span data-ttu-id="0cf8d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0cf8d-136">NOTES</span></span>
<span data-ttu-id="0cf8d-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="0cf8d-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0cf8d-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0cf8d-138">RELATED LINKS</span></span>
