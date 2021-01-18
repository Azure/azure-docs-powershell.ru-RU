---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b0e32d58d416fce869995595c3e2a2ff69e8f349
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516982"
---
# <span data-ttu-id="5d144-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5d144-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="5d144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d144-102">SYNOPSIS</span></span>
<span data-ttu-id="5d144-103">Создание и обновление выходных данных для задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d144-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="5d144-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d144-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d144-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d144-105">DESCRIPTION</span></span>
<span data-ttu-id="5d144-106">**Cmdlet New-AzStreamAnalyticsOutput** создает выходной результат в рамках задания Stream Analytics или обновляет существующий выход.</span><span class="sxs-lookup"><span data-stu-id="5d144-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="5d144-107">Имя выходных данных можно Укайл. JSON-файл или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="5d144-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="5d144-108">Если они заданы, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="5d144-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="5d144-109">Если указать выходной результат, который уже существует, а параметр *Force* не указан, будет указано, следует ли заменить существующий выход.</span><span class="sxs-lookup"><span data-stu-id="5d144-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="5d144-110">Если задать параметр *Force* и указать существующее выходное имя, выходные данные будут заменены без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5d144-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="5d144-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d144-111">EXAMPLES</span></span>

### <span data-ttu-id="5d144-112">Пример 1. Добавление результата в задание</span><span class="sxs-lookup"><span data-stu-id="5d144-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="5d144-113">Эта команда создает новый выходной результат под названием "Вывод в задание StreamingJob".</span><span class="sxs-lookup"><span data-stu-id="5d144-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="5d144-114">Если существующий выходной код с этим именем уже определен, будет выпроспрос установлена возможность замены.</span><span class="sxs-lookup"><span data-stu-id="5d144-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="5d144-115">Пример 2. Замена определения выходных данных задания</span><span class="sxs-lookup"><span data-stu-id="5d144-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="5d144-116">Эта команда заменяет определение output в задаче StreamingJob без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5d144-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="5d144-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d144-117">PARAMETERS</span></span>

### <span data-ttu-id="5d144-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d144-118">-DefaultProfile</span></span>
<span data-ttu-id="5d144-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d144-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d144-120">-File</span><span class="sxs-lookup"><span data-stu-id="5d144-120">-File</span></span>
<span data-ttu-id="5d144-121">Путь к файлу JSON, который содержит представление JSON результата Azure Stream Analytics, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="5d144-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="5d144-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5d144-122">-Force</span></span>
<span data-ttu-id="5d144-123">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5d144-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d144-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="5d144-124">-JobName</span></span>
<span data-ttu-id="5d144-125">Указывает имя задания Azure Stream Analytics, для которого создается выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d144-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="5d144-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5d144-126">-Name</span></span>
<span data-ttu-id="5d144-127">Указывает имя выходных данных Azure Stream Analytics, которые нужно создать.</span><span class="sxs-lookup"><span data-stu-id="5d144-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="5d144-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d144-128">-ResourceGroupName</span></span>
<span data-ttu-id="5d144-129">Имя группы ресурсов, для которой создается выход Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d144-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="5d144-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d144-130">-Confirm</span></span>
<span data-ttu-id="5d144-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d144-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d144-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d144-132">-WhatIf</span></span>
<span data-ttu-id="5d144-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d144-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d144-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5d144-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d144-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d144-135">CommonParameters</span></span>
<span data-ttu-id="5d144-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d144-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d144-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d144-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d144-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d144-138">INPUTS</span></span>

### <span data-ttu-id="5d144-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5d144-139">System.String</span></span>

## <span data-ttu-id="5d144-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d144-140">OUTPUTS</span></span>

### <span data-ttu-id="5d144-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="5d144-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="5d144-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d144-142">NOTES</span></span>

## <span data-ttu-id="5d144-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d144-143">RELATED LINKS</span></span>

[<span data-ttu-id="5d144-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5d144-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="5d144-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5d144-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="5d144-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="5d144-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


