---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: ed5b11684fdb8701343c9390962e95942f4075e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217044"
---
# <span data-ttu-id="26033-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="26033-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="26033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26033-102">SYNOPSIS</span></span>
<span data-ttu-id="26033-103">Создает или обновляет задание средства аналитики Stream.</span><span class="sxs-lookup"><span data-stu-id="26033-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="26033-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26033-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26033-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26033-105">DESCRIPTION</span></span>
<span data-ttu-id="26033-106">Для создания нового задания аналитики Stream в Azure или обновления определения существующего задания с его использованием будет установлено новое задание **AzStreamAnalyticsJob.**</span><span class="sxs-lookup"><span data-stu-id="26033-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="26033-107">Имя задания можно у указывает в области. JSON-файл или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="26033-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="26033-108">Если они заданы, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="26033-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="26033-109">Если указать существующее имя задания, а параметр *Force* не указан, будет выдан запрос на замену существующего задания.</span><span class="sxs-lookup"><span data-stu-id="26033-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="26033-110">Если задать параметр *Force* и указать существующее имя задания, определение задания будет заменено без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="26033-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="26033-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26033-111">EXAMPLES</span></span>

### <span data-ttu-id="26033-112">ПРИМЕР 1. Создание задания</span><span class="sxs-lookup"><span data-stu-id="26033-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="26033-113">Эта команда создает задание на основе определения в JobDefinition.js.</span><span class="sxs-lookup"><span data-stu-id="26033-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="26033-114">Если существующее задание с указанным именем в файле определения задания уже определено, будет выдан запрос на его замену.</span><span class="sxs-lookup"><span data-stu-id="26033-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="26033-115">ПРИМЕР 2. Замена определения задания</span><span class="sxs-lookup"><span data-stu-id="26033-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="26033-116">Эта команда заменяет определение задания для StreamingJob без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="26033-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="26033-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26033-117">PARAMETERS</span></span>

### <span data-ttu-id="26033-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26033-118">-DefaultProfile</span></span>
<span data-ttu-id="26033-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26033-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26033-120">-File</span><span class="sxs-lookup"><span data-stu-id="26033-120">-File</span></span>
<span data-ttu-id="26033-121">Путь к файлу JSON, который содержит представление JSON задания Azure Stream Analytics, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="26033-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26033-122">-Force</span><span class="sxs-lookup"><span data-stu-id="26033-122">-Force</span></span>
<span data-ttu-id="26033-123">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="26033-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26033-124">-Name</span><span class="sxs-lookup"><span data-stu-id="26033-124">-Name</span></span>
<span data-ttu-id="26033-125">Указывает имя задания аналитики Azure Stream Analytics, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="26033-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26033-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26033-126">-ResourceGroupName</span></span>
<span data-ttu-id="26033-127">Имя группы ресурсов, к которой относится задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="26033-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="26033-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26033-128">-Confirm</span></span>
<span data-ttu-id="26033-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="26033-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26033-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26033-130">-WhatIf</span></span>
<span data-ttu-id="26033-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26033-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26033-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="26033-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26033-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26033-133">CommonParameters</span></span>
<span data-ttu-id="26033-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26033-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26033-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26033-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26033-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26033-136">INPUTS</span></span>

### <span data-ttu-id="26033-137">System.String</span><span class="sxs-lookup"><span data-stu-id="26033-137">System.String</span></span>

## <span data-ttu-id="26033-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26033-138">OUTPUTS</span></span>

### <span data-ttu-id="26033-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="26033-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="26033-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26033-140">NOTES</span></span>

## <span data-ttu-id="26033-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26033-141">RELATED LINKS</span></span>

[<span data-ttu-id="26033-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="26033-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="26033-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="26033-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="26033-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="26033-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="26033-145">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="26033-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="26033-146">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="26033-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


