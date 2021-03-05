---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ac303b4e458e836238a148f1a33b009e9c0b0e24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973832"
---
# <span data-ttu-id="a5dff-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a5dff-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="a5dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5dff-102">SYNOPSIS</span></span>
<span data-ttu-id="a5dff-103">Создает или заменяет функцию в заданиях Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a5dff-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="a5dff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5dff-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5dff-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5dff-105">DESCRIPTION</span></span>
<span data-ttu-id="a5dff-106">С его использованием новая **функция AzStreamAnalyticsFunction** создается в задание аналитики Azure Stream Analytics или заменяется существующей.</span><span class="sxs-lookup"><span data-stu-id="a5dff-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="a5dff-107">Определите функцию в файле нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="a5dff-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="a5dff-108">Имя функции можно указать с помощью параметра *Name* или в JSON-файле.</span><span class="sxs-lookup"><span data-stu-id="a5dff-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="a5dff-109">Если указать имя в обоих способах, имена должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="a5dff-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="a5dff-110">Чтобы заменить существующую функцию, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="a5dff-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="a5dff-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5dff-111">EXAMPLES</span></span>

### <span data-ttu-id="a5dff-112">Пример 1. Создание функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="a5dff-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="a5dff-113">Эта команда создает функцию на основе Function07.jsфайла.</span><span class="sxs-lookup"><span data-stu-id="a5dff-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="a5dff-114">Имя функции хранится в JSON-файле.</span><span class="sxs-lookup"><span data-stu-id="a5dff-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="a5dff-115">Пример 2. Создание функции Stream Analytics с названием ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="a5dff-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="a5dff-116">Эта команда создает функцию для задания "ScoreTweet".</span><span class="sxs-lookup"><span data-stu-id="a5dff-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="a5dff-117">Пример 3. Замена функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="a5dff-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="a5dff-118">Эта команда заменяет определение существующей функции ScoreTweet определением в Function22.js.</span><span class="sxs-lookup"><span data-stu-id="a5dff-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="a5dff-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5dff-119">PARAMETERS</span></span>

### <span data-ttu-id="a5dff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5dff-120">-DefaultProfile</span></span>
<span data-ttu-id="a5dff-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5dff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5dff-122">-File</span><span class="sxs-lookup"><span data-stu-id="a5dff-122">-File</span></span>
<span data-ttu-id="a5dff-123">Путь к JSON-файлу, который содержит представление JSON функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a5dff-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dff-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a5dff-124">-Force</span></span>
<span data-ttu-id="a5dff-125">Указывает на то, что этот cmdlet заменяет существующую функцию Stream Analytics, не запросив подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a5dff-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a5dff-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="a5dff-126">-JobName</span></span>
<span data-ttu-id="a5dff-127">Указывает имя задания Stream Analytics, в котором этот cmdlet создает функцию Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a5dff-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5dff-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a5dff-128">-Name</span></span>
<span data-ttu-id="a5dff-129">Указывает имя функции Stream Analytics, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5dff-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5dff-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5dff-130">-ResourceGroupName</span></span>
<span data-ttu-id="a5dff-131">Указывает имя группы ресурсов, в которой этот cmdlet создает функцию Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a5dff-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5dff-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5dff-132">-Confirm</span></span>
<span data-ttu-id="a5dff-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5dff-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5dff-134">-WhatIf</span></span>
<span data-ttu-id="a5dff-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5dff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5dff-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a5dff-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5dff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5dff-137">CommonParameters</span></span>
<span data-ttu-id="a5dff-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5dff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5dff-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5dff-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5dff-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5dff-140">INPUTS</span></span>

### <span data-ttu-id="a5dff-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a5dff-141">System.String</span></span>

## <span data-ttu-id="a5dff-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5dff-142">OUTPUTS</span></span>

### <span data-ttu-id="a5dff-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="a5dff-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="a5dff-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5dff-144">NOTES</span></span>

## <span data-ttu-id="a5dff-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5dff-145">RELATED LINKS</span></span>

[<span data-ttu-id="a5dff-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a5dff-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="a5dff-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a5dff-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="a5dff-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="a5dff-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


