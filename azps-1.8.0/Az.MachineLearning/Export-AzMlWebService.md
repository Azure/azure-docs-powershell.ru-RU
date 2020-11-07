---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 02588ded441c1ac9f23deb19b763c099ce6c18ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899801"
---
# <span data-ttu-id="5a3de-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="5a3de-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="5a3de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a3de-102">SYNOPSIS</span></span>
<span data-ttu-id="5a3de-103">Экспортирует объект определения веб-службы в отформатированную строку в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="5a3de-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="5a3de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a3de-104">SYNTAX</span></span>

### <span data-ttu-id="5a3de-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="5a3de-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a3de-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="5a3de-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a3de-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a3de-107">DESCRIPTION</span></span>
<span data-ttu-id="5a3de-108">Экспортирует объект определения для указанной веб-servive в отформатированную строку JSON.</span><span class="sxs-lookup"><span data-stu-id="5a3de-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="5a3de-109">Вы можете вернуть строку немедленно или сохранить ее в файле.</span><span class="sxs-lookup"><span data-stu-id="5a3de-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="5a3de-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a3de-110">EXAMPLES</span></span>

### <span data-ttu-id="5a3de-111">Пример 1: экспорт в виде строки</span><span class="sxs-lookup"><span data-stu-id="5a3de-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="5a3de-112">Пример 2: экспорт в файл</span><span class="sxs-lookup"><span data-stu-id="5a3de-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="5a3de-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a3de-113">PARAMETERS</span></span>

### <span data-ttu-id="5a3de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a3de-114">-DefaultProfile</span></span>
<span data-ttu-id="5a3de-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5a3de-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a3de-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5a3de-116">-Force</span></span>
<span data-ttu-id="5a3de-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5a3de-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5a3de-118">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="5a3de-118">-OutputFile</span></span>
<span data-ttu-id="5a3de-119">Путь к файлу для экспортированного определения.</span><span class="sxs-lookup"><span data-stu-id="5a3de-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="5a3de-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="5a3de-120">-ToJsonString</span></span>
<span data-ttu-id="5a3de-121">Указывает, что определение будет экспортировано в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="5a3de-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="5a3de-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="5a3de-122">-WebService</span></span>
<span data-ttu-id="5a3de-123">Объект определения веб-службы, который необходимо экспортировать.</span><span class="sxs-lookup"><span data-stu-id="5a3de-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="5a3de-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a3de-124">-Confirm</span></span>
<span data-ttu-id="5a3de-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a3de-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a3de-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a3de-126">-WhatIf</span></span>
<span data-ttu-id="5a3de-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a3de-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a3de-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a3de-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a3de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a3de-129">CommonParameters</span></span>
<span data-ttu-id="5a3de-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a3de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a3de-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a3de-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a3de-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a3de-132">INPUTS</span></span>

### <span data-ttu-id="5a3de-133">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="5a3de-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="5a3de-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a3de-134">OUTPUTS</span></span>

### <span data-ttu-id="5a3de-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5a3de-135">System.String</span></span>

## <span data-ttu-id="5a3de-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a3de-136">NOTES</span></span>
<span data-ttu-id="5a3de-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="5a3de-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5a3de-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a3de-138">RELATED LINKS</span></span>
