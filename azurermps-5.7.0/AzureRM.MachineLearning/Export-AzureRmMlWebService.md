---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/export-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: fd07ab55fad93fdf48df52e15db846630ba6c1f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568574"
---
# <span data-ttu-id="999df-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="999df-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="999df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="999df-102">SYNOPSIS</span></span>
<span data-ttu-id="999df-103">Экспортирует объект определения веб-службы в отформатированную строку в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="999df-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="999df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="999df-104">SYNTAX</span></span>

### <span data-ttu-id="999df-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="999df-105">ExportToFile</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="999df-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="999df-106">ExportToJSON</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="999df-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="999df-107">DESCRIPTION</span></span>
<span data-ttu-id="999df-108">Экспортирует объект определения для указанной веб-servive в отформатированную строку JSON.</span><span class="sxs-lookup"><span data-stu-id="999df-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="999df-109">Вы можете вернуть строку немедленно или сохранить ее в файле.</span><span class="sxs-lookup"><span data-stu-id="999df-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="999df-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="999df-110">EXAMPLES</span></span>

### <span data-ttu-id="999df-111">--------------------------Пример 1: экспорт в виде строки--------------------------</span><span class="sxs-lookup"><span data-stu-id="999df-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="999df-112">--------------------------Пример 2: экспорт в файл--------------------------</span><span class="sxs-lookup"><span data-stu-id="999df-112">--------------------------  Example 2: Export to file  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="999df-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="999df-113">PARAMETERS</span></span>

### <span data-ttu-id="999df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="999df-114">-DefaultProfile</span></span>
<span data-ttu-id="999df-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="999df-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="999df-116">-Force</span><span class="sxs-lookup"><span data-stu-id="999df-116">-Force</span></span>
<span data-ttu-id="999df-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="999df-117">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999df-118">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="999df-118">-OutputFile</span></span>
<span data-ttu-id="999df-119">Путь к файлу для экспортированного определения.</span><span class="sxs-lookup"><span data-stu-id="999df-119">The file path for exported definition.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999df-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="999df-120">-ToJsonString</span></span>
<span data-ttu-id="999df-121">Указывает, что определение будет экспортировано в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="999df-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToJSON
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999df-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="999df-122">-WebService</span></span>
<span data-ttu-id="999df-123">Объект определения веб-службы, который необходимо экспортировать.</span><span class="sxs-lookup"><span data-stu-id="999df-123">The web service definition object to be exported.</span></span>

```yaml
Type: WebService
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="999df-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="999df-124">-Confirm</span></span>
<span data-ttu-id="999df-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="999df-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999df-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="999df-126">-WhatIf</span></span>
<span data-ttu-id="999df-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="999df-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="999df-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="999df-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999df-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="999df-129">CommonParameters</span></span>
<span data-ttu-id="999df-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="999df-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="999df-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="999df-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="999df-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="999df-132">INPUTS</span></span>

### <span data-ttu-id="999df-133">Вебслужба</span><span class="sxs-lookup"><span data-stu-id="999df-133">WebService</span></span>
<span data-ttu-id="999df-134">Параметр "WebService" принимает значение типа WebService из конвейера</span><span class="sxs-lookup"><span data-stu-id="999df-134">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="999df-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="999df-135">OUTPUTS</span></span>

### <span data-ttu-id="999df-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="999df-136">None</span></span>

## <span data-ttu-id="999df-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="999df-137">NOTES</span></span>
<span data-ttu-id="999df-138">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="999df-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="999df-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="999df-139">RELATED LINKS</span></span>

