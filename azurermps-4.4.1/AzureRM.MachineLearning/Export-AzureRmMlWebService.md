---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: f8923c6f98dad44a56c35cadc4b3e1daedeb1227
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566710"
---
# <span data-ttu-id="66387-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="66387-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="66387-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66387-102">SYNOPSIS</span></span>
<span data-ttu-id="66387-103">Экспортирует объект определения веб-службы в отформатированную строку в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="66387-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66387-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66387-104">SYNTAX</span></span>

### <span data-ttu-id="66387-105">Экспорт в файл.</span><span class="sxs-lookup"><span data-stu-id="66387-105">Export to file.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66387-106">Экспорт в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="66387-106">Export to JSON string.</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66387-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66387-107">DESCRIPTION</span></span>
<span data-ttu-id="66387-108">Экспортирует объект определения для указанной веб-servive в отформатированную строку JSON.</span><span class="sxs-lookup"><span data-stu-id="66387-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="66387-109">Вы можете вернуть строку немедленно или сохранить ее в файле.</span><span class="sxs-lookup"><span data-stu-id="66387-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="66387-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66387-110">EXAMPLES</span></span>

### <span data-ttu-id="66387-111">--------------------------Пример 1: экспорт в виде строки--------------------------</span><span class="sxs-lookup"><span data-stu-id="66387-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
<span data-ttu-id="66387-112">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="66387-112">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="66387-113">--------------------------Пример 2: экспорт в файл--------------------------</span><span class="sxs-lookup"><span data-stu-id="66387-113">--------------------------  Example 2: Export to file  --------------------------</span></span>
<span data-ttu-id="66387-114">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="66387-114">@{paragraph=PS C:\\\>}</span></span>





```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="66387-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66387-115">PARAMETERS</span></span>

### <span data-ttu-id="66387-116">-Force</span><span class="sxs-lookup"><span data-stu-id="66387-116">-Force</span></span>
<span data-ttu-id="66387-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="66387-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="66387-118">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="66387-118">-OutputFile</span></span>
<span data-ttu-id="66387-119">Путь к файлу для экспортированного определения.</span><span class="sxs-lookup"><span data-stu-id="66387-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66387-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="66387-120">-ToJsonString</span></span>
<span data-ttu-id="66387-121">Указывает, что определение будет экспортировано в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="66387-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to JSON string.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66387-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="66387-122">-WebService</span></span>
<span data-ttu-id="66387-123">Объект определения веб-службы, который необходимо экспортировать.</span><span class="sxs-lookup"><span data-stu-id="66387-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="66387-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66387-124">-Confirm</span></span>
<span data-ttu-id="66387-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="66387-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66387-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66387-126">-WhatIf</span></span>
<span data-ttu-id="66387-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="66387-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66387-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="66387-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66387-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66387-129">-DefaultProfile</span></span>
<span data-ttu-id="66387-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66387-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66387-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66387-131">CommonParameters</span></span>
<span data-ttu-id="66387-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66387-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66387-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66387-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66387-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66387-134">INPUTS</span></span>

### <span data-ttu-id="66387-135">Вебслужба</span><span class="sxs-lookup"><span data-stu-id="66387-135">WebService</span></span>
<span data-ttu-id="66387-136">Параметр "WebService" принимает значение типа WebService из конвейера</span><span class="sxs-lookup"><span data-stu-id="66387-136">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="66387-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66387-137">OUTPUTS</span></span>

### <span data-ttu-id="66387-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="66387-138">None</span></span>

## <span data-ttu-id="66387-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="66387-139">NOTES</span></span>
<span data-ttu-id="66387-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="66387-140">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="66387-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66387-141">RELATED LINKS</span></span>

