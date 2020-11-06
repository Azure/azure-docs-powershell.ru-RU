---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/export-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: 45e0fe4583477b05d4218f9e7b3ffb920b0218d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565398"
---
# <span data-ttu-id="5a0a0-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="5a0a0-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="5a0a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5a0a0-103">Экспортирует объект определения веб-службы в отформатированную строку в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a0a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a0a0-104">SYNTAX</span></span>

### <span data-ttu-id="5a0a0-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="5a0a0-105">ExportToFile</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a0a0-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="5a0a0-106">ExportToJSON</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a0a0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a0a0-107">DESCRIPTION</span></span>
<span data-ttu-id="5a0a0-108">Экспортирует объект определения для указанной веб-servive в отформатированную строку JSON.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="5a0a0-109">Вы можете вернуть строку немедленно или сохранить ее в файле.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="5a0a0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a0a0-110">EXAMPLES</span></span>

### <span data-ttu-id="5a0a0-111">Пример 1: экспорт в виде строки</span><span class="sxs-lookup"><span data-stu-id="5a0a0-111">Example 1: Export as string</span></span>
```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="5a0a0-112">Пример 2: экспорт в файл</span><span class="sxs-lookup"><span data-stu-id="5a0a0-112">Example 2: Export to file</span></span>
```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="5a0a0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a0a0-113">PARAMETERS</span></span>

### <span data-ttu-id="5a0a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a0a0-114">-DefaultProfile</span></span>
<span data-ttu-id="5a0a0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5a0a0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a0a0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5a0a0-116">-Force</span></span>
<span data-ttu-id="5a0a0-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5a0a0-118">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="5a0a0-118">-OutputFile</span></span>
<span data-ttu-id="5a0a0-119">Путь к файлу для экспортированного определения.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="5a0a0-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="5a0a0-120">-ToJsonString</span></span>
<span data-ttu-id="5a0a0-121">Указывает, что определение будет экспортировано в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="5a0a0-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="5a0a0-122">-WebService</span></span>
<span data-ttu-id="5a0a0-123">Объект определения веб-службы, который необходимо экспортировать.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="5a0a0-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a0a0-124">-Confirm</span></span>
<span data-ttu-id="5a0a0-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a0a0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a0a0-126">-WhatIf</span></span>
<span data-ttu-id="5a0a0-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a0a0-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a0a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a0a0-129">CommonParameters</span></span>
<span data-ttu-id="5a0a0-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a0a0-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a0a0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a0a0-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a0a0-132">INPUTS</span></span>

### <span data-ttu-id="5a0a0-133">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="5a0a0-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="5a0a0-134">Параметры: WebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5a0a0-134">Parameters: WebService (ByValue)</span></span>

## <span data-ttu-id="5a0a0-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a0a0-135">OUTPUTS</span></span>

### <span data-ttu-id="5a0a0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5a0a0-136">System.String</span></span>

## <span data-ttu-id="5a0a0-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a0a0-137">NOTES</span></span>
<span data-ttu-id="5a0a0-138">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5a0a0-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5a0a0-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a0a0-139">RELATED LINKS</span></span>
