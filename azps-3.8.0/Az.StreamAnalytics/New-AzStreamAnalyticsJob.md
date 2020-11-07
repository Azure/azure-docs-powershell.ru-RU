---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: ed5b11684fdb8701343c9390962e95942f4075e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912117"
---
# <span data-ttu-id="19d35-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="19d35-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="19d35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19d35-102">SYNOPSIS</span></span>
<span data-ttu-id="19d35-103">Создание или обновление задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="19d35-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="19d35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19d35-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19d35-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19d35-105">DESCRIPTION</span></span>
<span data-ttu-id="19d35-106">Командлет **New-AzStreamAnalyticsJob** создает новое задание Stream Analytics в Azure или обновляет определение существующего указанного задания.</span><span class="sxs-lookup"><span data-stu-id="19d35-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="19d35-107">Название задания можно задать в поле. Файл JSON или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="19d35-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="19d35-108">Если заданы оба флажка, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="19d35-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="19d35-109">Если вы указали уже существующее имя задания и не указали параметр *Force* , командлет задаст вопрос, нужно ли заменять существующее задание.</span><span class="sxs-lookup"><span data-stu-id="19d35-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="19d35-110">Если указать параметр *Force* и задать существующее имя задания, определение задания будет заменено без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="19d35-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="19d35-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19d35-111">EXAMPLES</span></span>

### <span data-ttu-id="19d35-112">Пример 1: создание задания</span><span class="sxs-lookup"><span data-stu-id="19d35-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="19d35-113">Эта команда создает задание из определения в JobDefinition.json.</span><span class="sxs-lookup"><span data-stu-id="19d35-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="19d35-114">Если существующее задание с указанным именем в файле определения задания уже определено, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="19d35-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="19d35-115">Пример 2: Замена определения задания</span><span class="sxs-lookup"><span data-stu-id="19d35-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="19d35-116">Эта команда заменяет определение задания для StreamingJob без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="19d35-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="19d35-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19d35-117">PARAMETERS</span></span>

### <span data-ttu-id="19d35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d35-118">-DefaultProfile</span></span>
<span data-ttu-id="19d35-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19d35-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19d35-120">-Файл</span><span class="sxs-lookup"><span data-stu-id="19d35-120">-File</span></span>
<span data-ttu-id="19d35-121">Задает путь к файлу JSON, содержащему представление JSON задания Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="19d35-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="19d35-122">-Force</span><span class="sxs-lookup"><span data-stu-id="19d35-122">-Force</span></span>
<span data-ttu-id="19d35-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="19d35-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="19d35-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19d35-124">-Name</span></span>
<span data-ttu-id="19d35-125">Указывает имя задания Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="19d35-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="19d35-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19d35-126">-ResourceGroupName</span></span>
<span data-ttu-id="19d35-127">Указывает имя группы ресурсов, которой должно принадлежать задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="19d35-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="19d35-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19d35-128">-Confirm</span></span>
<span data-ttu-id="19d35-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19d35-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19d35-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19d35-130">-WhatIf</span></span>
<span data-ttu-id="19d35-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19d35-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19d35-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19d35-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19d35-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d35-133">CommonParameters</span></span>
<span data-ttu-id="19d35-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19d35-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d35-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d35-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d35-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19d35-136">INPUTS</span></span>

### <span data-ttu-id="19d35-137">System. String</span><span class="sxs-lookup"><span data-stu-id="19d35-137">System.String</span></span>

## <span data-ttu-id="19d35-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19d35-138">OUTPUTS</span></span>

### <span data-ttu-id="19d35-139">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="19d35-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="19d35-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="19d35-140">NOTES</span></span>

## <span data-ttu-id="19d35-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19d35-141">RELATED LINKS</span></span>

[<span data-ttu-id="19d35-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="19d35-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="19d35-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="19d35-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="19d35-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="19d35-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="19d35-145">Остановить-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="19d35-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="19d35-146">Остановить-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="19d35-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


