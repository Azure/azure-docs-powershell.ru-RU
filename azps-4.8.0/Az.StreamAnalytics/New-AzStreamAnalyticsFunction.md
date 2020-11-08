---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 71a6267b06ce47ee36f220033ec598af3680deeb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077487"
---
# <span data-ttu-id="7b286-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7b286-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="7b286-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b286-102">SYNOPSIS</span></span>
<span data-ttu-id="7b286-103">Создает или заменяет функцию в задании Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7b286-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="7b286-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b286-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b286-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b286-105">DESCRIPTION</span></span>
<span data-ttu-id="7b286-106">Командлет **New-AzStreamAnalyticsFunction** создает функцию в задании Azure Stream Analytics или заменяет существующую функцию.</span><span class="sxs-lookup"><span data-stu-id="7b286-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="7b286-107">Определите функцию в файле нотации JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="7b286-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="7b286-108">Вы можете указать имя функции с помощью параметра *Name (имя* ) или в файле. JSON.</span><span class="sxs-lookup"><span data-stu-id="7b286-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="7b286-109">Если указать имя обоими способами, имена должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="7b286-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="7b286-110">Чтобы заменить существующую функцию, укажите имя существующей функции.</span><span class="sxs-lookup"><span data-stu-id="7b286-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="7b286-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b286-111">EXAMPLES</span></span>

### <span data-ttu-id="7b286-112">Пример 1: создание функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="7b286-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="7b286-113">Эта команда создает функцию из файла Function07.json.</span><span class="sxs-lookup"><span data-stu-id="7b286-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="7b286-114">Имя функции хранится в JSON – файле.</span><span class="sxs-lookup"><span data-stu-id="7b286-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="7b286-115">Пример 2: создание функции Stream Analytics с именем ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="7b286-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="7b286-116">Эта команда создает функцию для задания с именем ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="7b286-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="7b286-117">Пример 3: замена функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="7b286-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="7b286-118">Эта команда заменяет определение существующей функции с именем ScoreTweet с определением в Function22.json.</span><span class="sxs-lookup"><span data-stu-id="7b286-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="7b286-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b286-119">PARAMETERS</span></span>

### <span data-ttu-id="7b286-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b286-120">-DefaultProfile</span></span>
<span data-ttu-id="7b286-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b286-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b286-122">-Файл</span><span class="sxs-lookup"><span data-stu-id="7b286-122">-File</span></span>
<span data-ttu-id="7b286-123">Указывает путь JSON-файла, который содержит представление JSON функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7b286-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="7b286-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7b286-124">-Force</span></span>
<span data-ttu-id="7b286-125">Указывает на то, что этот командлет заменяет существующую функцию Stream Analytics без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7b286-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7b286-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="7b286-126">-JobName</span></span>
<span data-ttu-id="7b286-127">Указывает имя задания Stream Analytics, в соответствии с которым этот командлет создает функцию Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7b286-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="7b286-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b286-128">-Name</span></span>
<span data-ttu-id="7b286-129">Указывает имя функции Stream Analytics, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7b286-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7b286-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b286-130">-ResourceGroupName</span></span>
<span data-ttu-id="7b286-131">Указывает имя группы ресурсов, в которой этот командлет создает функцию Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7b286-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="7b286-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b286-132">-Confirm</span></span>
<span data-ttu-id="7b286-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7b286-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b286-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b286-134">-WhatIf</span></span>
<span data-ttu-id="7b286-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7b286-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b286-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b286-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b286-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b286-137">CommonParameters</span></span>
<span data-ttu-id="7b286-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b286-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b286-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b286-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b286-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b286-140">INPUTS</span></span>

### <span data-ttu-id="7b286-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7b286-141">System.String</span></span>

## <span data-ttu-id="7b286-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b286-142">OUTPUTS</span></span>

### <span data-ttu-id="7b286-143">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="7b286-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="7b286-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b286-144">NOTES</span></span>

## <span data-ttu-id="7b286-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b286-145">RELATED LINKS</span></span>

[<span data-ttu-id="7b286-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7b286-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="7b286-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7b286-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="7b286-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7b286-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)

