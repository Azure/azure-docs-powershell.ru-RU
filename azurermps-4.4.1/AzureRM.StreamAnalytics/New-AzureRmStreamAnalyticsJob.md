---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 5d56c0523077ee8a45b2a41175ca54c5a0e10907
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569151"
---
# <span data-ttu-id="ad985-101">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ad985-101">New-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="ad985-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad985-102">SYNOPSIS</span></span>
<span data-ttu-id="ad985-103">Создание или обновление задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ad985-103">Creates or updates a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad985-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad985-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad985-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad985-105">DESCRIPTION</span></span>
<span data-ttu-id="ad985-106">Командлет **New-AzureRmStreamAnalyticsJob** создает новое задание Stream Analytics в Azure или обновляет определение существующего указанного задания.</span><span class="sxs-lookup"><span data-stu-id="ad985-106">The **New-AzureRmStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="ad985-107">Название задания можно задать в поле. Файл JSON или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="ad985-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="ad985-108">Если заданы оба флажка, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="ad985-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="ad985-109">Если вы указали уже существующее имя задания и не указали параметр *Force* , командлет задаст вопрос, нужно ли заменять существующее задание.</span><span class="sxs-lookup"><span data-stu-id="ad985-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>

<span data-ttu-id="ad985-110">Если указать параметр *Force* и задать существующее имя задания, определение задания будет заменено без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ad985-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="ad985-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad985-111">EXAMPLES</span></span>

### <span data-ttu-id="ad985-112">Пример 1: создание задания</span><span class="sxs-lookup"><span data-stu-id="ad985-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="ad985-113">Эта команда создает задание из определения в JobDefinition.json.</span><span class="sxs-lookup"><span data-stu-id="ad985-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="ad985-114">Если существующее задание с указанным именем в файле определения задания уже определено, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="ad985-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="ad985-115">Пример 2: Замена определения задания</span><span class="sxs-lookup"><span data-stu-id="ad985-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="ad985-116">Эта команда заменяет определение задания для StreamingJob без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ad985-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="ad985-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad985-117">PARAMETERS</span></span>

### <span data-ttu-id="ad985-118">-Файл</span><span class="sxs-lookup"><span data-stu-id="ad985-118">-File</span></span>
<span data-ttu-id="ad985-119">Задает путь к файлу JSON, содержащему представление JSON задания Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="ad985-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="ad985-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ad985-120">-Force</span></span>
<span data-ttu-id="ad985-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad985-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad985-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad985-122">-Name</span></span>
<span data-ttu-id="ad985-123">Указывает имя задания Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="ad985-123">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="ad985-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad985-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad985-125">Указывает имя группы ресурсов, которой должно принадлежать задание Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ad985-125">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="ad985-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad985-126">-Confirm</span></span>
<span data-ttu-id="ad985-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad985-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad985-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad985-128">-WhatIf</span></span>
<span data-ttu-id="ad985-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad985-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad985-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad985-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad985-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad985-131">-DefaultProfile</span></span>
<span data-ttu-id="ad985-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad985-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad985-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad985-133">CommonParameters</span></span>
<span data-ttu-id="ad985-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad985-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad985-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad985-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad985-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad985-136">INPUTS</span></span>

## <span data-ttu-id="ad985-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad985-137">OUTPUTS</span></span>

### <span data-ttu-id="ad985-138">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="ad985-138">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="ad985-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad985-139">NOTES</span></span>

## <span data-ttu-id="ad985-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad985-140">RELATED LINKS</span></span>

[<span data-ttu-id="ad985-141">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ad985-141">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="ad985-142">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ad985-142">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="ad985-143">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ad985-143">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="ad985-144">Остановить-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ad985-144">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="ad985-145">Остановить-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ad985-145">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


