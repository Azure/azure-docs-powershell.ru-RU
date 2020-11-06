---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 6b05bb1d379a5d9072cc286505a507d3718aa33e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563816"
---
# <span data-ttu-id="4b567-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4b567-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="4b567-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b567-102">SYNOPSIS</span></span>
<span data-ttu-id="4b567-103">Создает или заменяет функцию в задании Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="4b567-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b567-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b567-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b567-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b567-105">DESCRIPTION</span></span>
<span data-ttu-id="4b567-106">Командлет **New-AzureRmStreamAnalyticsFunction** создает функцию в задании Azure Stream Analytics или заменяет существующую функцию.</span><span class="sxs-lookup"><span data-stu-id="4b567-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="4b567-107">Определите функцию в файле нотации JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="4b567-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="4b567-108">Вы можете указать имя функции с помощью параметра *Name (имя* ) или в файле. JSON.</span><span class="sxs-lookup"><span data-stu-id="4b567-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="4b567-109">Если указать имя обоими способами, имена должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="4b567-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="4b567-110">Чтобы заменить существующую функцию, укажите имя существующей функции.</span><span class="sxs-lookup"><span data-stu-id="4b567-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="4b567-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b567-111">EXAMPLES</span></span>

### <span data-ttu-id="4b567-112">Пример 1: создание функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="4b567-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="4b567-113">Эта команда создает функцию из файла Function07.json.</span><span class="sxs-lookup"><span data-stu-id="4b567-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="4b567-114">Имя функции хранится в JSON – файле.</span><span class="sxs-lookup"><span data-stu-id="4b567-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="4b567-115">Пример 2: создание функции Stream Analytics с именем ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="4b567-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="4b567-116">Эта команда создает функцию для задания с именем ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="4b567-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="4b567-117">Пример 3: замена функции Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="4b567-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="4b567-118">Эта команда заменяет определение существующей функции с именем ScoreTweet с определением в Function22.json.</span><span class="sxs-lookup"><span data-stu-id="4b567-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="4b567-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b567-119">PARAMETERS</span></span>

### <span data-ttu-id="4b567-120">-Файл</span><span class="sxs-lookup"><span data-stu-id="4b567-120">-File</span></span>
<span data-ttu-id="4b567-121">Указывает путь JSON-файла, который содержит представление JSON функции Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="4b567-121">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="4b567-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4b567-122">-Force</span></span>
<span data-ttu-id="4b567-123">Указывает на то, что этот командлет заменяет существующую функцию Stream Analytics без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4b567-123">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4b567-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="4b567-124">-JobName</span></span>
<span data-ttu-id="4b567-125">Указывает имя задания Stream Analytics, в соответствии с которым этот командлет создает функцию Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="4b567-125">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="4b567-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4b567-126">-Name</span></span>
<span data-ttu-id="4b567-127">Указывает имя функции Stream Analytics, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4b567-127">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4b567-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b567-128">-ResourceGroupName</span></span>
<span data-ttu-id="4b567-129">Указывает имя группы ресурсов, в которой этот командлет создает функцию Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="4b567-129">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="4b567-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b567-130">-Confirm</span></span>
<span data-ttu-id="4b567-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b567-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b567-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b567-132">-WhatIf</span></span>
<span data-ttu-id="4b567-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b567-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b567-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b567-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b567-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b567-135">-DefaultProfile</span></span>
<span data-ttu-id="4b567-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b567-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b567-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b567-137">CommonParameters</span></span>
<span data-ttu-id="4b567-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b567-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b567-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b567-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b567-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b567-140">INPUTS</span></span>

## <span data-ttu-id="4b567-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b567-141">OUTPUTS</span></span>

### <span data-ttu-id="4b567-142">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="4b567-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="4b567-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b567-143">NOTES</span></span>

## <span data-ttu-id="4b567-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b567-144">RELATED LINKS</span></span>

[<span data-ttu-id="4b567-145">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4b567-145">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="4b567-146">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4b567-146">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="4b567-147">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4b567-147">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


