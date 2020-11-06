---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 540ea984d165a841288d1928192ad0ce035f7eb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565313"
---
# <span data-ttu-id="da079-101">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="da079-101">New-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="da079-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da079-102">SYNOPSIS</span></span>
<span data-ttu-id="da079-103">Создание или обновление задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="da079-103">Creates or updates a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da079-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da079-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da079-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da079-105">DESCRIPTION</span></span>
<span data-ttu-id="da079-106">Командлет **New-AzureRmStreamAnalyticsJob** создает новое задание Stream Analytics в Azure или обновляет определение существующего указанного задания.</span><span class="sxs-lookup"><span data-stu-id="da079-106">The **New-AzureRmStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="da079-107">Название задания можно задать в поле. Файл JSON или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="da079-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="da079-108">Если заданы оба флажка, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="da079-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="da079-109">Если вы указали уже существующее имя задания и не указали параметр *Force* , командлет задаст вопрос, нужно ли заменять существующее задание.</span><span class="sxs-lookup"><span data-stu-id="da079-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="da079-110">Если указать параметр *Force* и задать существующее имя задания, определение задания будет заменено без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="da079-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="da079-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da079-111">EXAMPLES</span></span>

### <span data-ttu-id="da079-112">Пример 1: создание задания</span><span class="sxs-lookup"><span data-stu-id="da079-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="da079-113">Эта команда создает задание из определения в JobDefinition.json.</span><span class="sxs-lookup"><span data-stu-id="da079-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="da079-114">Если существующее задание с указанным именем в файле определения задания уже определено, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="da079-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="da079-115">Пример 2: Замена определения задания</span><span class="sxs-lookup"><span data-stu-id="da079-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="da079-116">Эта команда заменяет определение задания для StreamingJob без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="da079-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="da079-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da079-117">PARAMETERS</span></span>

### <span data-ttu-id="da079-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da079-118">-DefaultProfile</span></span>
<span data-ttu-id="da079-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da079-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da079-120">-Файл</span><span class="sxs-lookup"><span data-stu-id="da079-120">-File</span></span>
<span data-ttu-id="da079-121">Задает путь к файлу JSON, содержащему представление JSON задания Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="da079-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="da079-122">-Force</span><span class="sxs-lookup"><span data-stu-id="da079-122">-Force</span></span>
<span data-ttu-id="da079-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="da079-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da079-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da079-124">-Name</span></span>
<span data-ttu-id="da079-125">Указывает имя задания Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="da079-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="da079-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da079-126">-ResourceGroupName</span></span>
<span data-ttu-id="da079-127">Указывает имя группы ресурсов, которой должно принадлежать задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="da079-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="da079-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da079-128">-Confirm</span></span>
<span data-ttu-id="da079-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da079-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da079-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da079-130">-WhatIf</span></span>
<span data-ttu-id="da079-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da079-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da079-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da079-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da079-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da079-133">CommonParameters</span></span>
<span data-ttu-id="da079-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da079-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da079-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da079-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da079-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da079-136">INPUTS</span></span>

### <span data-ttu-id="da079-137">System. String</span><span class="sxs-lookup"><span data-stu-id="da079-137">System.String</span></span>

## <span data-ttu-id="da079-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da079-138">OUTPUTS</span></span>

### <span data-ttu-id="da079-139">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="da079-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="da079-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="da079-140">NOTES</span></span>

## <span data-ttu-id="da079-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da079-141">RELATED LINKS</span></span>

[<span data-ttu-id="da079-142">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="da079-142">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="da079-143">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="da079-143">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="da079-144">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="da079-144">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="da079-145">Остановить-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="da079-145">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="da079-146">Остановить-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="da079-146">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


