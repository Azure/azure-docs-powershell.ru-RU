---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: cb92753e151aa274c17c678a1d4316260242f32c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556468"
---
# <span data-ttu-id="49e53-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="49e53-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="49e53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49e53-102">SYNOPSIS</span></span>
<span data-ttu-id="49e53-103">Создает или заменяет функцию в задании Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="49e53-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49e53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49e53-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49e53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49e53-105">DESCRIPTION</span></span>
<span data-ttu-id="49e53-106">Командлет **New-AzureRmStreamAnalyticsFunction** создает функцию в задании Azure Stream Analytics или заменяет существующую функцию.</span><span class="sxs-lookup"><span data-stu-id="49e53-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="49e53-107">Определите функцию в файле нотации JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="49e53-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="49e53-108">Вы можете указать имя функции с помощью параметра *Name (имя* ) или в файле. JSON.</span><span class="sxs-lookup"><span data-stu-id="49e53-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="49e53-109">Если указать имя обоими способами, имена должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="49e53-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="49e53-110">Чтобы заменить существующую функцию, укажите имя существующей функции.</span><span class="sxs-lookup"><span data-stu-id="49e53-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="49e53-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49e53-111">EXAMPLES</span></span>

### <span data-ttu-id="49e53-112">Пример 1: создание функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="49e53-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="49e53-113">Эта команда создает функцию из файла Function07.json.</span><span class="sxs-lookup"><span data-stu-id="49e53-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="49e53-114">Имя функции хранится в JSON – файле.</span><span class="sxs-lookup"><span data-stu-id="49e53-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="49e53-115">Пример 2: создание функции Stream Analytics с именем ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="49e53-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="49e53-116">Эта команда создает функцию для задания с именем ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="49e53-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="49e53-117">Пример 3: замена функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="49e53-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="49e53-118">Эта команда заменяет определение существующей функции с именем ScoreTweet с определением в Function22.json.</span><span class="sxs-lookup"><span data-stu-id="49e53-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="49e53-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49e53-119">PARAMETERS</span></span>

### <span data-ttu-id="49e53-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e53-120">-DefaultProfile</span></span>
<span data-ttu-id="49e53-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49e53-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49e53-122">-Файл</span><span class="sxs-lookup"><span data-stu-id="49e53-122">-File</span></span>
<span data-ttu-id="49e53-123">Указывает путь JSON-файла, который содержит представление JSON функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="49e53-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="49e53-124">-Force</span><span class="sxs-lookup"><span data-stu-id="49e53-124">-Force</span></span>
<span data-ttu-id="49e53-125">Указывает на то, что этот командлет заменяет существующую функцию Stream Analytics без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="49e53-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="49e53-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="49e53-126">-JobName</span></span>
<span data-ttu-id="49e53-127">Указывает имя задания Stream Analytics, в соответствии с которым этот командлет создает функцию Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="49e53-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="49e53-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49e53-128">-Name</span></span>
<span data-ttu-id="49e53-129">Указывает имя функции Stream Analytics, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="49e53-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="49e53-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e53-130">-ResourceGroupName</span></span>
<span data-ttu-id="49e53-131">Указывает имя группы ресурсов, в которой этот командлет создает функцию Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="49e53-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="49e53-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49e53-132">-Confirm</span></span>
<span data-ttu-id="49e53-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49e53-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49e53-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49e53-134">-WhatIf</span></span>
<span data-ttu-id="49e53-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49e53-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49e53-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49e53-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49e53-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e53-137">CommonParameters</span></span>
<span data-ttu-id="49e53-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49e53-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e53-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e53-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e53-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49e53-140">INPUTS</span></span>

### <span data-ttu-id="49e53-141">System. String</span><span class="sxs-lookup"><span data-stu-id="49e53-141">System.String</span></span>

## <span data-ttu-id="49e53-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49e53-142">OUTPUTS</span></span>

### <span data-ttu-id="49e53-143">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="49e53-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="49e53-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="49e53-144">NOTES</span></span>

## <span data-ttu-id="49e53-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49e53-145">RELATED LINKS</span></span>

[<span data-ttu-id="49e53-146">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="49e53-146">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="49e53-147">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="49e53-147">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="49e53-148">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="49e53-148">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


