---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: f2d9d2b53d07380e3bdb0a97ea3f3e70107ee0a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561988"
---
# <span data-ttu-id="bd4d1-101">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bd4d1-101">New-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="bd4d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd4d1-103">Создает или обновляет выходные данные для задания Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-103">Creates or updates outputs for a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd4d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd4d1-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd4d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd4d1-105">DESCRIPTION</span></span>
<span data-ttu-id="bd4d1-106">Командлет **New-AzureRmStreamAnalyticsOutput** создает выходные данные в задании Stream Analytics или обновляет существующий вывод.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-106">The **New-AzureRmStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="bd4d1-107">Имя выходных данных можно задать в поле. Файл JSON или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="bd4d1-108">Если заданы оба флажка, имя в командной строке должно совпадать с именем в файле.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="bd4d1-109">Если вы укажете уже существующий и не указали параметр *Force* , командлет задаст вопрос, нужно ли заменить существующий вывод.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>

<span data-ttu-id="bd4d1-110">Если указать параметр *Force* и задать существующее выходное имя, выходные данные будут заменены без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="bd4d1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd4d1-111">EXAMPLES</span></span>

### <span data-ttu-id="bd4d1-112">Пример 1: Добавление выходных данных к заданию</span><span class="sxs-lookup"><span data-stu-id="bd4d1-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="bd4d1-113">Эта команда создает новый вывод с именем Output в задании с именем StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="bd4d1-114">Если существующий выход с этим именем уже определен, командлет задаст вопрос, нужно ли его заменить.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="bd4d1-115">Пример 2: Замена определения вывода задания</span><span class="sxs-lookup"><span data-stu-id="bd4d1-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="bd4d1-116">Эта команда заменяет определение для вывода в задании с именем StreamingJob без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="bd4d1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd4d1-117">PARAMETERS</span></span>

### <span data-ttu-id="bd4d1-118">-Файл</span><span class="sxs-lookup"><span data-stu-id="bd4d1-118">-File</span></span>
<span data-ttu-id="bd4d1-119">Задает путь к файлу JSON, содержащему представление JSON выходных данных Azure Stream Analytics для создания.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="bd4d1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bd4d1-120">-Force</span></span>
<span data-ttu-id="bd4d1-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bd4d1-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="bd4d1-122">-JobName</span></span>
<span data-ttu-id="bd4d1-123">Указывает имя задания Azure Stream Analytics, в котором нужно создать выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-123">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="bd4d1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd4d1-124">-Name</span></span>
<span data-ttu-id="bd4d1-125">Указывает имя создаваемого вывода Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-125">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="bd4d1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd4d1-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd4d1-127">Указывает имя группы ресурсов, в которой нужно создать выходные данные Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-127">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="bd4d1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd4d1-128">-Confirm</span></span>
<span data-ttu-id="bd4d1-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd4d1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd4d1-130">-WhatIf</span></span>
<span data-ttu-id="bd4d1-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd4d1-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd4d1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd4d1-133">-DefaultProfile</span></span>
<span data-ttu-id="bd4d1-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd4d1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd4d1-135">CommonParameters</span></span>
<span data-ttu-id="bd4d1-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd4d1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd4d1-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd4d1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd4d1-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd4d1-138">INPUTS</span></span>

## <span data-ttu-id="bd4d1-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd4d1-139">OUTPUTS</span></span>

### <span data-ttu-id="bd4d1-140">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="bd4d1-140">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="bd4d1-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd4d1-141">NOTES</span></span>

## <span data-ttu-id="bd4d1-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd4d1-142">RELATED LINKS</span></span>

[<span data-ttu-id="bd4d1-143">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bd4d1-143">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="bd4d1-144">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bd4d1-144">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="bd4d1-145">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bd4d1-145">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


